# File Systems and Allocation Methods

This file explains how data is stored, organized, and accessed on disk through physical and logical structures. It also describes file allocation strategies used by operating systems.

---

## Physical vs Logical Disk Structure

### Physical Disk Structure
- Made up of **platters** coated with magnetic material
- Data is organized into:
  - **Tracks**: Concentric circles on platters
  - **Cylinders**: Same track across multiple platters
  - **Sectors**: Subdivisions of tracks (usually 512 bytes)

**Disk arms** move read/write heads across platters, while the platter spins to locate sectors.

### Logical Disk Structure
- Focuses on how the operating system views and manages data:
  - **Partitions**: Independent logical segments (e.g., C: drive, D: drive)
  - **Drives**: Labels for partitions
  - **Blocks**: Fixed-size units used for reading/writing

---

## File Allocation Methods

Allocation refers to how file data is assigned to blocks on disk. Three main strategies exist:

### 1. Contiguous Allocation
- Each file occupies blocks placed one after another
- OS stores the starting block and file length
- Example:
  - Start block = 2, Length = 2
  - End block = 2 + 2 - 1 = 3

**Advantages:**
- Easy to implement
- Fast for sequential and random access
- Minimal head movement

**Disadvantages:**
- Hard to expand files
- Causes **external fragmentation**
- Difficult to find large contiguous space

**Access Efficiency:**
- If the location is known → O(1)
- If unknown → N/2 average block reads

---

### 2. Chained (Linked) Allocation
- File blocks are scattered but linked using pointers
- Directory stores start block and length
- Last block has an EOF (end-of-file) marker

**Advantages:**
- No file size limit
- Easier to allocate space
- No external fragmentation

**Disadvantages:**
- No random access (only sequential)
- Slower due to pointer-following
- Extra space used for pointers

**Access Efficiency:**
- Best case: 1 access
- Average case: N/2
- Worst case: N

---

### 3. Indexed Allocation (Inode)
- Each file has an **index block** storing pointers to data blocks
- Inode (index node) maps a file to multiple blocks

**Example:**
- File 11 → blocks: 10, 25, 2, 16, 82, 20

**Multilevel Indexing:**
- Index blocks can point to other index blocks (tree structure)
- Used in UNIX-based systems

**Access Time:**
- Logarithmic (O(log₂N)) using multilevel index
- Example: 16 blocks → log₂(16) = 4 max accesses

**Advantages:**
- No fragmentation
- Direct access to blocks
- Good for large files

**Disadvantages:**
- Uses more space
- Complex structure

---

## Summary: File Access Complexity

| Allocation Type | Access Time        | Random Access | Fragmentation |
|------------------|---------------------|----------------|----------------|
| Contiguous       | O(1)                | Yes            | Yes            |
| Linked           | O(N), avg N/2       | No             | No             |
| Indexed/Inode    | O(log₂N)            | Yes            | No             |

---

## Real-World Usage

- **FAT (File Allocation Table)** uses linked allocation
- **NTFS** and **ext3/ext4 (Linux)** use indexed allocation
- Modern systems use hybrid approaches

This concludes your notes on file systems and allocation strategies.
