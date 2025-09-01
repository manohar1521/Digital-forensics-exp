# Experiment 1 : Create a forensic image of a storage device's using FTK Imager.

## 🎯 Aim
The aim is to create a forensically sound, bit-by-bit copy (or "image") of a storage device without altering the original evidence. This is done using FTK Imager, a free, standalone software from Exterro. The image file includes all data, such as active and deleted files, unallocated space, and file system structures, ensuring a complete and verifiable replica of the original evidence for legal and investigative purposes.

## 📝 Description
FTK Imager is a widely used digital forensics tool that allows investigators to preview data on a storage device and create a perfect duplicate. This process, known as imaging, is crucial for preserving the integrity of digital evidence. By creating an image, forensic examiners can analyze the copy rather than the original, protecting the evidence's chain of custody. The software also automatically generates a cryptographic hash of the data, which serves as a unique fingerprint to prove the image's authenticity.

## 🛠️ Tools & Equipment Used
FTK Imager Software: A free application for data preview and forensic imaging.

Forensic Workstation: A computer with enough storage and processing power for the task.

Target Storage Device: The device being imaged (e.g., hard drive, USB drive).

Hardware Write Blocker: A physical device that prevents any data from being written to the original evidence drive. This is the single most critical tool for preserving data integrity.

Destination Storage Device: An empty hard drive or network location with sufficient space to store the forensic image. It should be at least as large as the source device.

## ⚙️ Procedure
Connect the Target Device: Connect the evidence drive to the forensic workstation via a write blocker.
![alt text](<Screenshots/Screenshot 2025-09-01 204903.png>)
Launch FTK Imager: Open the FTK Imager application.
![alt text](<Screenshots/Screenshot 2025-09-01 205027.png>)
Start Imaging: Go to the "File" menu and select "Create Disk Image." Choose "Physical Drive" as the source.
![alt text](<Screenshots/Screenshot 2025-09-01 205204.png>)
Select Drive: From the list, select the physical drive you want to image. Use the drive's serial number or model to confirm it's the correct one.
![alt text](<Screenshots/Screenshot 2025-09-01 205220.png>)
Add Destination: Click "Add" to specify where the image will be saved. Choose an image type (e.g., E01 for compressed images with metadata or Raw/DD for a simple bit-by-bit copy).
![alt text](<Screenshots/Screenshot 2025-09-01 205220.png>)
Enter Case Information: Provide the case number, evidence number, and a description. This information is embedded in the image file and is vital for maintaining the chain of custody.
![alt text](<Screenshots/Screenshot 2025-09-01 205616.png>)
Start Process: Click "Start" to begin. FTK Imager will create the image and compute a hash of the data.
![alt text](<Screenshots/Screenshot 2025-09-01 210124.png>)
Verification: After completion, FTK Imager will perform a verification step, calculating the hash of the created image and comparing it to the hash of ![alt text](<Screenshots/Screenshot 2025-09-01 195839.png>)the original source drive.

## ✅ Result
The result is a forensically sound image file stored on the destination drive. FTK Imager generates a report confirming that the hash values of the original drive and the created image file match. This hash verification is a crucial step that cryptographically proves the image is an exact, unaltered replica of the original evidence. The report, along with the documented chain of custody, ensures the image is admissible as evidence in legal proceedings.