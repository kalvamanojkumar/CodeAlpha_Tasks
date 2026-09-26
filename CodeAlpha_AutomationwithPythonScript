import os
import shutil

# Source and destination folders
source_folder = "source_folder"
destination_folder = "destination_folder"

# Create destination folder if it doesn't exist
if not os.path.exists(destination_folder):
    os.makedirs(destination_folder)

# Go through all files in the source folder
for filename in os.listdir(source_folder):

    # Check if the file is a JPG file
    if filename.lower().endswith(".jpg"):
        source_path = os.path.join(source_folder, filename)
        destination_path = os.path.join(destination_folder, filename)

        # Move the file
        shutil.move(source_path, destination_path)

        print("Moved:", filename)

print("All JPG files have been moved successfully!")
