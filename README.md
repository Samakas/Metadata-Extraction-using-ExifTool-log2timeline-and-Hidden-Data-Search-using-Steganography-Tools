# Metadata-Extraction-using-ExifTool-log2timeline-and-Hidden-Data-Search-using-Steganography-Tools
### Name: Samakash R S
### Reg NO: 212223230182

## AIM:
To extract metadata, perform timeline analysis, and search for hidden data using forensic tools like ExifTool, log2timeline, and steganography detection tools.

## DESIGN STEPS:
### Step 1:
Use exiftool to extract metadata from files such as images, documents, and videos.

### Step 2:
Use log2timeline and plaso to create and analyze event timelines from system logs and file metadata.

### Step 3:
Apply steganography detection tools like steghide, zsteg, or binwalk to uncover hidden data in media files.

## PROGRAM:
Metadata and Timeline Forensics, Steganography Analysis Steps

## OUTPUT:
# A. Using ExifTool – for file metadata

 Install:
```
sudo apt update
sudo apt install exiftool -y
```
 Extract metadata from a file:
```
exiftool image.jpg
```
 Batch process a folder:
```
exiftool -r /path/to/folder
```
Useful flags:

-G: Show metadata group

-time:all: Show only timestamps

-GPSLatitude -GPSLongitude: Extract GPS data

![img01](https://github.com/user-attachments/assets/25459619-0989-4212-9232-f43bcabdcedb)


# install log2timeline
```
sudo apt install plaso -y
```
```
sudo apt install steghide -y
```
# Embed data
```
steghide embed -cf /home/kali/Downloads/wallpaper.jpg -ef /home/kali/Downloads/secret.txt
```
![image](https://github.com/user-attachments/assets/47166c87-4abe-4226-9529-141f1f602ec9)

Extract hidden data:
```
steghide extract -sf hidden.jpg
```
![image](https://github.com/user-attachments/assets/f7d8e853-d26b-4226-93f2-ccd5d73b9de3)

# Using binwalk – for file analysis

```
sudo apt install binwalk -y
binwalk suspicious.jpg
```
![image](https://github.com/user-attachments/assets/7fcc7fe9-bf17-47e5-9405-3800b294a7ea)


## RESULT:
Metadata was successfully extracted, timeline analysis was completed, and hidden data was identified using steganography tools.

