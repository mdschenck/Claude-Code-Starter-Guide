## Custom Rug Quote Tracker

### User Story: 
- As a Jaipur Living Custom Rugs sales associate, I want to have a tool to track the custom rug quoting process from initial consultation request until custom rug sku creation so that I can keep track of custom rug orders, follow up with the customer on outstanding steps, and have a clear overview of all current open custom projects in flight. 
- As a Jaipur Living customer that is ordering a custom rug, I want a simple customer facing portal that will show me all of my open custom orders current status, renderings of CAD designs, and any outstanding items needed to complete the order. 

### Requirements - Business Functionality & Acceptance Criteria
- Custom rugs database that tracks each custom inquiry and includes the following fields: 
  - Quote Number - Unique, incrementing starting with CRQ000001
  - Customer Name
  - Customer Number
  - Customer Company
  - CAD File Link (URL)
  - Image Render Link (URL)
  - Quote Status
     - Quote Status Values:
     - Inquiry
     - Accepted
     - Cad Created
     - Swatch Ordered
     - Swatch Creation
     - Swatch Shipped
     - Swatch Approval Pending
     - Swatch Approved
     - Order Created
     - On Loom
     - Finishing
     - In Transit
     - Complete
  - Sales Order Number
  - Custom Rug SKU

- New database entries will be created with a webhook or event observer on a form entry on the Jaipur Living website that will be a front end component only. This tool will work outside of the JL website, but the front end user interface will be presented to the customer in a iFrame embed as a MVP/ Proof of concept.

- When a new quote is created, only the unique quote ID, Customer Name, Customer Number, and Customer Company will be populated from the web form. The rest of the fields will be populated by the Jaipur Living Custom Team.
  
- Front End customer UI (To be hosted outside of the jaipur living website, but show as a web embed iFrame) that allows the customer to see their open quotes, with all database fields presented in an easy, intuitive table interface. Image Render links should display as thumbnails in the table for easy reference.

- Back End Admin UI that allows Jaipur Living associates to add information to fields for created quotes as the custom rug proceeds through the custom rug creation process.  This admin portal should have a simple login.  
	- The back end UI should also allow Jaipur Living associates to create new quote lines with a button to "Create New Quote". This will also allow us to test the UI functionality while the webhook or form submit event listener scripts are being created.

### Front End Design 
- Front End Customer interface design should match the Jaipur Living MY ORDERS page for the custom orders table, with all colors, fonts, font sizes, etc matched as closely as possible.  A screengrab of the page as well as the HTML code snippet of the table can be found in the \reference-files directory.  
- Use the UI/UX Max skill to assist in the design, favoring the simplest, most intuitive interface.