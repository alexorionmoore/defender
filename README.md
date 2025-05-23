# defender
Chicago Defender Work

# Subfolders
- An XML with a large amount of metadata about the other files contained in the folder. Metadata includes such important things as:
  - Date of publication
  - Page of the newspaper
  - Grouping ID?
  - Actual data about the content of the image, in one case the text of an ad??
  - Issue ID
  - The type of thing contained, like advertisement?
- A set of .002 extension files, which seem to be the actual extractable images
- A ZONEMAP.300 folder, which seems to have data on how the different .002 files are connected, and in particular the rectangular coordinates for what part of the newspaper page was cut out to obtain each component image

So far, it seems like basically every distinct segment of the newspaper gets its own well-described file. Basically, storing huge data in tons of tiny files with lots and lots of reconstructive metadata. 

The command "magick <filepath.002> <path-to-new-image.png>" seems to be sufficient to convert every single 002 file into the relevant .png. 


# PAGES folder
- PAGELIST.xml is uninteresting
- Seems to show which pages are contained in the subfolders of the directories. Each page is associated with a .300, .302, .002, and .004 file. The .002 and .004 are typically extractable images, which is curious
- The .300 and .302 files seem to list which subfolders (by name) should be collated to form the relevant page. They also list lots of metadata that would seem useful for how to take the images from these subfolders and collate them, i.e. top/bottom/left/right coordinates for each of a large number of zones within the page. 

## Plan
- It seems like the first step will be to extract a single subfolder. Once I can confidently extract the images, and maintain their association with the relevant metadata, then I can look at using the data in PAGES to collate them.

## Notes
Wow! These files are from like, ... 2006