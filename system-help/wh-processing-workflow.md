---
title: "Processing Workflow for Long and Flat Products"
source: "madcap.md"
tags: ["4GL", "Help Documentation"]
version: "1.0"
last_updated: "2026-02-19"
short_description: "Processing Workflow for Long and Flat Products"
long_description: "Help documentation for Processing Workflow for Long and Flat Products in the 4GL system."
---

Processing Workflow for Long and Flat Products
==============================================

The following functions are typically used in processing long and flat products.

Print the sheet of barcodes for quick access to actions.

Processing Long Products
------------------------

![](../Resources/Images/Processing Workflow_Longs.png)

1. Log Transfer — Use this function to pick long products for processing machine.

   Scan the bundle you are picking from and enter the quantity you are taking from the bundle. This will give you a new log number and a label for the picked material. In the following example Log L001000 was scanned, the current quantity is displayed (11), and then the amount being picked is entered (6). This has now changed the quantity in Log L001000 to 5 and created a new log for the picked 6.

   ![](../Resources/Images/WH_log_transfer.png)

   Use the Log Transfer Reversal function if necessary to “unpick” a log.

   It is very important for tracing processed material correctly that you place the new label on the picked material, and that each pick is clearly marked separately. Do not mix material picked from two different bundles without clearly labeling them separately.
2. Linear Nesting Log Split — Once material has been picked for processing and is ready to be loaded on the machine, use this function to process long products.
   1. Scan the barcode for the line on the production order you are about to process:

   ![](../Resources/Images/WH_prod_order_section_barcode.png)

   2. Scan the label on the material to bring up the details of that material. Enter the quantity that you will cut. In example above we need to cut one length so we would enter 1; if you are pack cutting, enter the quantity in the pack.

   ![](../Resources/Images/WH_lin_nest_log_split1.png)

   3. All the cut pieces expected on that nest are displayed. The default is what’s expected, but you can press F6 to change:  
      Length (type length in mm)  
      Pcs  
      O – dictates if the cut piece will go to the order: 1=yes, 0=no  
      L – the number of labels needed

   ![](../Resources/Images/WH_lin_nest_log_split2.png)

   If there is an error and a RTS length is required, press F5 to enter a new line for the RTS.

   4. Press F3 and choose one of the following options: [revise with verbiage from Linear Nesting Log Split once it is finalized]  
      “1=All” or “0=Spl”– This completes the cut and gives you labels  
      “2=Edit” – Go back into the nest and change details  
      “3=Abt” – Abort, exits and clears without completing  
      “4=Use” – Not used by SSG
3. Log Split — If there is an error during the previous step and an additional feed length is required to be cut, change the nested expectation in Linear Nesting Log Split and then use this function to cut the remaining piece(s) from a new length.
   1. Scan the sales order number that corresponds to the production order line.
   2. Scan the log that you will be cutting the pieces from. If the sales order has multiple cut lengths of that product (e.g. CMS 100 x 14.8, 1 @ 2370 and 1 @ 2590), you will be prompted to select the line you are cutting. After selecting, you will see a message stating “Log Not Reserved for Line; OK?”; press Enter to continue.
   3. Line 1 defaults to the balance to be cut for the order, and line 2 defaults to the balance of the length. It assumes you wish to return that to stock:

   ![](../Resources/Images/WH_proc_log_split1.png)

   Change both lines to reflect what is being cut. In our example we want to cut 1 piece at 2370 to replace a damaged piece, and return a 9000 piece to stock.

   ![](../Resources/Images/WH_proc_log_split2.png)

   4. Press F3 to process [repeat step 2d above once it is finalized].

Processing Flat Products
------------------------

![](../Resources/Images/Processing Workflow_Plates.png)

1. The feed plate must be scanned during picking, then must be scanned on the bed.
   1. Choose the Conf Production & SigmaNEST Program function.
   2. Scan your production order (Job Traveller). The handheld will display the production order number and defaults to the feed plate that was assigned during programming.

      ![](../Resources/Images/WH_proc_flat_proc1.png)   
      ![](../Resources/Images/WH_proc_flat_proc2.png)
   3. Scan the feed plate you are actually picking. You must scan either the plate that was assigned during programming or a plate that is the same grade, thickness, width and length as the original plate.

      * If you picked the originally assigned plate, the handheld will display the plate details; simply press Enter in the OK field:

        ![](../Resources/Images/WH_proc_flat_proc3.png)
      * If you scan another plate that has the same grade and dimension, you will be prompted to confirm the swap before displaying the plate details. Note this plate number change on the production order:

        ![](../Resources/Images/WH_proc_flat_proc4.png)
      * If you pick a plate that does not have the same grade or dimension, the handheld will reject your pick. You will see an error “Product Mismatch; OK?”; press Enter to try again with another plate.
2. Once the feed plate is on the bed, launch the Update SigmaNEST IP function to process the flat products.
   1. Scan the production order. Details of the production order will be displayed.
   2. Once the plate has completed cutting:  
      If there was an error during cutting, press Esc: the job must be re-programmed before you can produce labels.  
      If there were no errors, press Enter to produce the labels.

Bundles and Labels
------------------

[Do you want to keep all these detailed here, or just listed with links to the existing component topics?]  
1. Packing  
2. Print Shipping Label  
3. Log Inquiry  
4. Location Change  
5. Log Label Reprint  
6. Printer Change

[The order above is per the SSG document; is the order important, or can we:  
- combine 1, 3, 4 as Managing Bundles  
- combine 2, 5, 6 as Reprinting Labels  
And perhaps even move both sections out of this topic into separate topics?]

1. If you need to create packages outside of the picking process (i.e. bundling after already picking, or bundling processed pieces), use the Package Maintenance function.

   **Scenario A - individual pieces are labelled.** For example, we have an order for some cut RHS 100 x 100 x 3, one piece 4m, one piece 3m, and one piece 1m. We have processed the material and put a shipping label on each piece.

   1. Enter the Run ID, then scan STRTPKG.
   2. Leave the Tot field blank and press Enter.
   3. In the Action field, scan each piece you are putting into the bundle.

   ![](../Resources/Images/WH_proc_pkg_mnt1.png)

   4. Once all are scanned, scan ENDPKG to produce a package label that displays the weight and quantity:

   ![](../Resources/Images/WH_proc_pkg_mnt2.png)

   **Scenario B - packaging small pieces that are loaded to drums or skids.** For example, we have cut 100 pieces of 30 x 30 x 3 angle into 30m pieces that we are going to pack into two drums. We won’t know how many is in each drum.

   1. Enter the Run ID, then scan STRTPKG.
   2. In theTot field, enter the number of skids/bundles you are packing.
   3. In theTyp field, record the type of package: the default is bundles; if you are packing on a skid, drum, etc. scan that barcode in this field. This field appears on the loading report.
   4. [next steps? Original doc goes directly from scenario description to label images]

   ![](../Resources/Images/WH_proc_pkg_mnt3.png) ![](../Resources/Images/WH_proc_pkg_mnt4.png)
2. If you need to reprint damaged or missing shipping labels, use the Shipping Labels function (see Tip below).
   1. Select option 1-Heat and press Enter.
   2. Scan your picking slip, then indicate if you want to print all or just one label. If you choose to only print one label, you will be prompted for the log number: remember that the initial letter must be uppercase.
3. If you want to know what the status of a bundle is (e.g. allocated to an order, downgrade, etc.), use the Log Inquiry function. Scan the inventory label to see the details.
4. If you are moving a bundle from one location in the warehouse to another, use the Location Change function to change the bin location. Scan the inventory label on the bundle you are moving, then scan the barcode of the bin location you are moving the bundle to.
5. If you need to reprint an inventory label, use the Log Label Reprint function. Either scan the label to be replaced, or manually type in the number (remember to enter letters uppercase) and press Enter.

Before printing labels, you must make sure your handheld will print to the right label printer.   
- Choose the Set Operator Default Label Printer [xref] function.   
- Use your barcode sheet to scan whether you’re changing for Shipping labels (need to do process for both barcodes), pick for processing & log label reprint.  
- Scan the barcode for the printer you want to use (printed on the label printer).  
- Press Enter through the Copies field and choose OK to return to the main menu.

---