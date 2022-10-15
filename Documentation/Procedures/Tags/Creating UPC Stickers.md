# Creating UPC Stickers
This document outlines steps taken to produce a PDF document of UPC labels for printing on a sheet of envelope label stickers.
    ![Mailing and Labels location](images/UPCLabels/1.png?raw=true)

We will be using Microsoft Word to create the document layout and formatting
### Create Layout
- Open Microsoft Word and create a blank document
- **Go-To** *Mailings*->*Labels*
- Input Item ID and Description in the Address Field
- Wrap Item ID in a pair of "*" (*Required for barcode font to work*)
- Choose the label you want to format for (*we are using Avery 5167*)
- Click *New Document*

### Format Labels
- Select All (ctrl+A)
- Center Text (Also good time to adjust font size based on label)
- Select all Item IDs with * terminators
  - (ctrl+F) -> *Input Item ID with * terminators*   
  - Access the search feild pulldown menu and choose *Advaced Find...*
  - Choose *Find in*->*Main Document*
 
You should now have all the instances of your item ID highlighed and can change the font to a barcode
While the item IDs are still selected, adjust your font size to fit the label, bigger is usually better for scannability.

## Save as PDF
- Bring up Print Dialog (ctrl+P)
- Choose *Microsoft Print to PDF* and hit Print
- You should be presented with a Save Dialog
- Save your PDF
## Print from PDF
- Open your PDF in Adobe Acrobat
- Bring up Print Dialog (ctrl+P)
- Choose *\\COCO\NORTH COPIER BW*
- Under **Page Sizing & Handling** Choose *Actual Size*
- Click *Properties* Button and chose the printer side tray by clicking the tray in the printer illustration and hit *OK*
- Load your labels in the tray facing down and hit print!
