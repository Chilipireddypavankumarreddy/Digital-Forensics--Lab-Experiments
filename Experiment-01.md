# Experiment 1: Evidence Acquisition Using AccessData FTK Imager

## Aim

To acquire a forensic disk image from a physical storage device using AccessData FTK Imager and verify the integrity of the acquired image using MD5 and SHA1 hash values.

## Software Used

- AccessData FTK Imager 4.7.1.2
- Windows

## Introduction

FTK Imager is a computer forensic tool developed by AccessData. It is used for acquiring and analyzing digital forensic evidence.

FTK Imager can acquire:

- Volatile memory (RAM)
- Non-volatile memory such as hard disks and USB drives
- Physical drives
- Logical drives
- Image files
- Contents of folders
- CDs/DVDs

In this experiment, a physical USB storage device was acquired and converted into a forensic disk image.

## Procedure

### Step 1: Open FTK Imager

Open **AccessData FTK Imager 4.7.1.2**.

Navigate to the option for creating a disk image.

<img width="342" height="241" alt="image" src="https://github.com/user-attachments/assets/35a7e1f2-d9a1-47f1-bf40-36c5ec0e8cf1" />


### Step 2: Select Evidence Source

Select **Physical Drive** and click **Next**.
<img width="679" height="550" alt="image" src="https://github.com/user-attachments/assets/77c9589a-ad6b-4f1d-8fb8-bc126b6f9087" />

### Step 3: Select Physical Drive

Select the physical drive that needs to be acquired.

The device used in this experiment was:

**SanDisk Cruzer Blade USB Device**

Click **Finish**.

### Step 4: Select Image Type

Select **Raw (dd)** and click **Next**.

<img width="679" height="543" alt="image" src="https://github.com/user-attachments/assets/faaf3161-6355-4ac7-9841-c8fc48c50214" />

### Step 5: Enter Evidence Information

The following evidence information was entered:

- Case Number: 1
- Evidence Number: 1
- Unique Description: DF
- Examiner: PAVAN KUMAR REDDY
- Notes: EXP 1

Click **Next**.
<img width="1462" height="1076" alt="image" src="https://github.com/user-attachments/assets/1589bc13-3ba2-4759-a1da-c4ccaed3efcc" />

### Step 6: Select Image Destination

The image was saved in the following destination:

`D:\3-1\Digital Forens

Image Filename:

`diskimage`

Image Fragment Size:

`0 MB`
<img width="702" height="598" alt="image" src="https://github.com/user-attachments/assets/129f830d-25eb-40ae-879d-496902488c84" />

### Step 7: Create Image

The source and destination information were displayed.

The option **Verify images after they are created** was selected.

Click **Start** to begin the acquisition.

<img width="651" height="387" alt="image" src="https://github.com/user-attachments/assets/11df82bd-3520-40d8-a53c-0c0727412f68" />

<img width="618" height="442" alt="image" src="https://github.com/user-attachments/assets/0d0d6620-a9d3-4f7f-af10-0162f2bc9fd9" />

### Step 8: Image Acquisition

FTK Imager started creating the forensic image from the physical drive.

<img width="1600" height="453" alt="image" src="https://github.com/user-attachments/assets/8a1b0499-d469-4902-a4e2-e839411e7788" />

### Step 9: Image Verification

After acquisition, FTK Imager verified the created forensic image.

The verification process checks the integrity of the acquired image using hash values.

### Step 10: Verification Result

The verification result showed:

- MD5 Verify Result: **Match**
- SHA1 Verify Result: **Match**
- Bad Blocks: **No bad blocks found in image**

### Step 11: Image Summary

The image summary provided details about the acquired physical drive.

Important information included:

- Source Type: Physical
- Drive Model: SanDisk Cruzer Blade USB Device
- Drive Interface Type: USB
- Source Data Size: 59112 MB
- Sector Count: 121061376
- Bytes per Sector: 512

### Step 12: Hash Verification

The image summary showed that the computed and reported hash values matched.

**MD5:**

`9f1f7659712cde7bc536dd82f341b5ce`

**SHA1:**

`abaca319c85c310078f410c02f6b11951af63334`

Both verification results were **Match**.

<img width="619" height="643" alt="image" src="https://github.com/user-attachments/assets/8a4a75aa-c8ff-4fa4-bbd5-0e80696c4dca" />

## Result

The physical USB drive was successfully acquired using **AccessData FTK Imager 4.7.1.2** and converted into a **Raw (dd) forensic image**.

The acquired image was successfully verified using MD5 and SHA1 hash values.

## Verification Results

| Parameter | Result |
|---|---|
| Image Type | Raw (dd) |
| Source | Physical Drive |
| Device | SanDisk Cruzer Blade USB Device |
| Source Size | 59112 MB |
| MD5 Verification | Match |
| SHA1 Verification | Match |
| Bad Blocks | No bad blocks found 



**Therefore, the forensic image was successfully created and its integrity was verified using MD5 and SHA1 hash values.**
