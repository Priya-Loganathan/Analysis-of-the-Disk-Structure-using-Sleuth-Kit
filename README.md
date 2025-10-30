# Analysis-of-the-Disk-Structure-using-Sleuth-Kit
## AIM:
To analyze the disk structure of a given disk image using Sleuth Kit tools in Kali Linux.

## DESIGN STEPS:
### Step 1:
Obtain or create a disk image file (e.g., disk.dd) to analyze. Open the terminal in Kali Linux.

### Step 2:
Use Sleuth Kit tools like mmls, fsstat, and fls to examine the partition layout, file system details, and file listing.

### Step 3:
Interpret the output of the tools to understand the disk structure, including partitions, sectors, and files.

## PROGRAM:
Sleuth Kit Disk Analysis Commands

✅ Option 1: Create a Sample Disk Image (for Testing)

Let’s create a 10MB blank disk image and simulate file system activity:

```bash
cd ~/Downloads

# Step 1: Create an empty disk image
dd if=/dev/zero of=disk.dd bs=1M count=10

# Step 2: Format it with a file system (like FAT32)
mkfs.vfat disk.dd
```

## OUTPUT:

<img width="647" height="126" alt="image" src="https://github.com/user-attachments/assets/0307cdf4-3768-4eff-b584-36c2097a791d" />

### Create Disk

<img width="487" height="132" alt="image" src="https://github.com/user-attachments/assets/4cb1035f-a6f3-4de1-893d-55b2e0ed9ab4" />

### mmls 
```bash
mmls disk.dd
```
### fls
```bash
fls -f fat -o 0 disk.dd
```
<img width="406" height="103" alt="image" src="https://github.com/user-attachments/assets/ead557d9-c61b-48a2-89c4-54398496750c" />

<img width="563" height="422" alt="image" src="https://github.com/user-attachments/assets/5e227a8d-e00e-42c2-ab52-d149f60e5ec7" />

## RESULT:
The analysis was performed successfully using Sleuth Kit, and the disk structure was understood in detail.
