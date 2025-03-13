# pdpditxx
my first iText application based on my iText testing code
I renamed it to pdpditxx.7 because it is iText 7. I am updating it to .net 9 and iText 9 and will load that here too.

I used all the different things I tried in my iText7 app, and tried to put them together in a way that you could run it with a zip file. 
This way, I can have the configuration options in a JSON file, and put that in a zip, and choose which thing it will do.
I am still pretty new at this, so if anyone has suggestions on better ways to do this, that would be great !
For now, it is run the exe, and add the zip file name as an arg, and it will unzip and do which thing you set true in the JSON.

An example of the json : 

{
  "Author": "RideBikes",
  "Date": "03/13/2025",
  "Description": "iText9 Code for PDF Processing",
  "EnableDebug": false,
  "Notes": "Concatenate a zip of PDF's in order of external index",
  "ProcessingActions": {
    "Concatenate": true,
    "MakeCopies": false,
    "ScaleAndRotate": false,
    "SmartSave": false,
    "Split": false,
    "TextConvert": false
  },
  "Settings": {
    "Concatenation": {
      "AddDocBreak": true,
      "BreakText": "DOC_BREAK"
    },
    "MakeCopies": {
      "NumberOfCopies": 20
    },
    "SmartSaving": {
      "StripComments": false,
      "FlattenAcroforms": false,
      "RemovePassword": false
    },
    "TargetPageSize": {
      "PageHeight": 792,
      "PageWidth": 612
    }
  }
}
