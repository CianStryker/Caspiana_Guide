# Omeka Guide
In our website we use a few specific features to build the  site. We use exhibits, simple pages, and items. Alongside these categories, we also use the default homepage given by the "DH @ Harvard" theme and a few plugins to customize the experience. 

# Exhbits & Simple Pages

# Items

# Homepage

# Themes

# Plugins
There are a variety of plugins available for Omeka to customize our site. All plugins can be installed, activated, or deactivated by clicking on the "Plugins" tab at the top of the admin page in Omeka. We used the following plugins: CSS Editor, CSV Import, Exhibit Builder, Harvard Key, Hide Elements, and Simple Pages. 

The CSS Editor plugin is the most complicated of these plugins and has its own sectin in the [repo](https://github.com/CianStryker/Caspiana_Guide/tree/main/Omeka%20Website%20Guide/CSS%20and%20Html%20Guide). The Exhibit Builder and Simple Pages plugins essentially allow you to use exhbits and simple pages. Harvard Key allows Harvard students to sign in as admins using thier Harvard credentials. And Hide Elements is useful for simplifying what information is available in the item pages. 

The CSV Import plugin is very important because that is how you upload the spreadsheet version of CASPIANA into Omeka. When you want to input the spreadsheet version, first make sure it is saves as a csv file. Then use the CSV Import page in Omeka and simply choose that file on your computer. Check the "Automap Column Names to Elements" tage and make sure under "Select Item Type" you select website. Click on "Make All Items Public?" to simplify things later. Ignore everything else and hit next. 

After hitting next, you should be on the "Step 2: Map COlumns to Elements, Tags, or Files" page. The only rows that are important are the "Dublin Core:" rows, "tags" and "Item Type Metadata:Local URL" rows. You can ingore "URL" and "Embedded Links". For the rows you do care about though, make sure that the "Map to Element" column in Omeka matches each identity, i.e. the "Dublic Core: Title" should have the element "Title" etc. Make sure you click on "Use HTML?" for each entry (not URL or Embedded Links since we don't care about those in Omeka). Also make sure you click on "Tags?" for the tags row. Then you can simply hit "Import CSV File" and the spreadsheet version of Caspiana will be inputted into Omeka. 
