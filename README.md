# Labelprinting
print multiple labels from google spreadsheets

Introduction
At this moment we use the program zebraprintdesigner for labeling units. This same information is also written down in google sheets which will be used for futher logistics. We would like to make this proces faster and easier and futurerpoof. Besides we have units that needs to be registered. Those units needs to have their own registration number that when dispatched will be connected to a label and at some point released from the label. For the registration we would like to use a barcodesystem
Printing labels per cliënt
For labeling we use Z4M and the S4M Zebra printers.
Each print assignment is per cliënt for labeling units.

Interface could be look like:
shows date and time
selection of [cliënt]
write down amount [totalunitnumber]
write down amount [unitspecial]
shows button and exit button

There are 2 departments labeling with different specs:

Labelspecification A
  [date] [time]
  [cliënt] Selected from google sheets or manual
  [unitAnumber] The number of the first label is "1" second label is "2"
  [totalunitAnumber] this number is the total amount of labels printed and the total amound of labels
  [unitAspecial] this number is on every label the same 
  [label-barcode] Includes: [client][date][time][unitAnumber]

Labelspecification B 
  [date] [time]
  [cliënt] Selected from google sheets or manual
  [unitBnumber] The number of the first label is "1" second label is "2"
  [totalunitBnumber] this number is the total amount of labels printed and the total amound of labels
  [unitBspecial] this number is on every label the same 
  [label-barcode] Includes: [client][date][time][unitBnumber]

Database connection
per client row per [date][time] in google sheets
-[totalunitAnumber] needs to be written to google sheets in  for example colum C connected to the row of [cliënt] rolleddown to [date][time]
-[totalunitBnumber] needs to be written to google sheets in for example colum D connected to the row of [cliënt] rolleddown to [date][time]
-[unitAspecial] needs to be written to google sheets in for example colum E connected to the row of [cliënt] rolleddown to [date][time]
-[unitBspecial] needs to be written to ggogle sheets in for example colum F connected to the row of [cliënt] rolleddown to [date][time]
