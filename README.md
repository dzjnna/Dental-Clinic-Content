# Dental-Clinic-Content

DASHBOARD - INFO ABOUT DENTAL CLINIC
PATIENT INFO - PATIENT ID, PATIENT NAME, AGE, ADDRESS, CONTACT NUMBER, EMAIL, GENDER, DOCTORS INFO(NAME, CONTACT)
APPOINTNENT- PATIENT NAME, DATE&TIME, SERVICE(KUNG ANONG GAGAWIN EX. CLEANING, PASTA, BUNOT), PRICE, STATUS(EX. DONE OR HINDI PA),
INVENTORY- ITEM, QUANTITY ON HAND(KUNG ILAN NALANG NATITIRA), UNIT COST, LAST ORDER DATE, 
BILLING- PATIENT NAME, GENDER, AGE, ADDRESS, DATE, CONTACT, EMAIL, PAYMENT METHOD(CASH OR E-WALLET) DOCTOR NAME, DESCRIPTION(KUNG ANO PINAGAWA NYA), PRICE, AMOUNT, TOTAL AMOUNT, SPACE FOR SIGNATURE OF DOCTOR OR STAFF
TREATMENT PLAN- TREATMENT PROCEDURE(KUNG ANONG GAGAWIN ROOT CANAL, CROWN ETC.), TOOTH NUMBER AND AREA(UPPER OR LOWER LEFT OR RIGHT), PRICE
VIEW-


ETO YUNG MGA FEATURES NG BAWAT CONTENT IKAW NAGBIGAY NETO PART MO TO SA PROPOSAL LAGAY KO NALANG DITO

Features: 
Patient Registration/Patient Information Form 
Fields:
•	Full Name
•	Date of Birth
•	Gender
•	Marital Status
•	Contact Numbers
•	Email Address
•	Residential Address
•	Emergency Contact Name and Number
•	Relationship to Emergency Contact

Functionality:
•	Unique Patient Id 
•	Basic Validation (Required fields, Correct format for Phone No and Email)
•	Editable fields for updating, and deleting the patient personal details

2.  Appointment
Fields:
•	Appointment Date and Time 
•	Dentist/Dental Practitioner
•	Reason for Visit
•	Status (Scheduled, Completed, Canceled)

Functionality:
•	Link to detailed appointment records 
•	Able to update or change the appointment scheduling system

3.  Billing
Fields:
•	Patient ID: Unique identifier for the patient
•	Name: Full name of the patient
•	Date of Birth: Patient’s birth date
•	Gender: Patient’s Gender
•	Contact Information: Phone number and email address 
•	Address: Home address of the patient

Billing Details:
Fields:
•	Billing Date: Date when the bill is issued	.
•	Invoice Number: Unique identifier for the invoice.	
•	Service Date: Date when the dental service was provided.
•	Procedure Code: Code for the specific dental procedure or treatment.
•	Procedure Description: Description of the dental procedure or treatment.
•	Quantity: Number of units or sessions of the procedure.
•	Unit Price: Price per unit of the procedure.
•	Total Amount: Total cost for the procedures or treatments.
•	Discounts: Any discounts applied to the total amount 
•	Tax Amount: Tax applied to the total amount, if applicable 
•	Grand Total: Final Amount due after discounts and taxes.

                         Functionality:
•	Includes all transactions, outstanding balances, and payment history for the patient’s references.
•	Payment Information:
•	Payment Method: Method of payment (e.g., cash, e-wallet).
•	Payment Amount: Amount paid by the patient or insurance.







4. Inventory
Dental Materials
Fields:
Fillings & Restorative Materials
•	Composite resins.
•	Amalgam.
•	Glass ionomer cement.

         Impression Materials
•	Alginate.
•	Polyvinyl siloxane.

                         Bonding Agents 
•	Etching gel.
•	Dental adhesives.

                                Dental Instruments 
                            Diagnostic Instruments 
•	Mouth mirrors.
•	Probes (explorers).
•	Tweezers (cotton pliers).

                     Hand Instruments 
•	Scalers.
•	Curettes.
•	Excavators.

                    Restorative Instrument
•	Burnishers.
•	Carvers.
•	Amalgam carriers.

                     Surgical Instruments
•	Forceps (extraction).
•	Scalpels.
•	Elavators.

                    Dental Equipment 
                       Handpieces
•	High-speed hand pieces.
•	Low-speed hand pieces.
•	Ultrasonic scalers.


Sterilization Equipment
•	Autoclave.
•	Ultrasonic cleaner.
•	Sterilization pouches.

                                Consumables 

Personal Protective Equipment (PPE)
•	Gloves.
•	Masks.
•	Gowns.
•	Face shields.

Disposables 
•	Cotton rolls.
•	Gauze pads.
•	Saliva ejectors.
•	Bibs & bib clips.

Medications 

Local Anesthetics
•	Lidocaine.
•	Articaine.

Antibiotics
•	Amoxicillin.
•	Clindamycin.

Pain Relief
•	Ibuprofen.
•	Acetaminophen.

Office Supplies 
•	Patient forms.
•	Appointment cards.
•	Printer ink/toner.
•	Paper.

Maintenance Supplies 
•	Hand piece lubricant.
•	Autoclave cleaner.
•	Disinfectants (surface, instrument).

Functionality:
•	It helps a dental clinic manage its inventory efficiently and monitor always available supplies for patient care.

5. Treatment Plan
   Fields:
•	Patient Details: Name, contact information, and other basic information about the patient,
•	Diagnosis: Description of the dental issues that need treatment.
•	Proposed Treatment: A summary of suggested actions accompanied by a brief explanation.
•	Progress Tracking: Capacity to keep track of treatment completion and make necessary plan updates



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <link href="https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css"  rel="stylesheet"/>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">

    <title>Treatment Plan</title>
</head>
<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body {
  background-color: #F0EFF4;
  background-repeat: no-repeat;
  background-size: cover;
  height: 100vh;
  margin: 0;
}

.main {
  display: grid;
  gap: 14px; /* Gap between items */
  margin: 14px; /* Margin around the grid */
  grid-template-columns: 1fr; /* Single column layout */
  grid-template-rows: auto 1fr; /* Auto size for header, flexible size for content */
  grid-template-areas:
    "header"
    "slideshow";
}

.content-header {
  grid-area: header;
}

.slideshow-container {
  grid-area: slideshow;
  position: relative; /* For positioning dots */
}

.text-center {
  text-align: center;
}

.dot {
  height: 15px;
  width: 15px;
  margin: 0 2px;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
  transition: background-color 0.6s ease;
}

.dot.active {
  background-color: #717171;
}

.mySlides {
  display: none; /* Hidden by default */
}

.fade {
  animation: fade 1.5s ease-in-out infinite;
}

@keyframes fade {
  0% { opacity: 0.5; }
  50% { opacity: 1; }
  100% { opacity: 0.5; }
}

.sidebar {
  position: fixed;
  top: 0;
  left: 0;
  height: 100%;
  background-color: #324376;
  color: #fff;
  padding: 25px;
  transition: all 0.3s;
} 

.sidebar-header {
  padding: 20px;
  background-color: #324376;
}

.sidebar ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.sidebar ul li {
  padding: 10px;
  border-bottom: 1px solid #444;
}

.sidebar ul li a {
  color: #fff;
  text-decoration: none;
}

.sidebar ul li a:hover {
  color: #ccc;
}

.sidebar ul ul {
  padding: 0;
  margin: 0;
  background-color: #333;
}

.sidebar ul ul li {
  padding: 10px;
  border-bottom: 1px solid #444;
}

.sidebar ul ul li a {
  color: #fff;
  text-decoration: none;
}

.sidebar ul ul li a:hover {
  color: #ccc;
}

.content {
  margin-left: 250px;
  padding: 20px;
}

#sidebarToggle {
  position: absolute;
  top: 10px;
  left: 10px;
  z-index: 1;
}
.sidebar {
  width: 250px;
}

.content {
  margin-left: 250px;
}

/* Tablet layout (max-width: 768px) */
@media only screen and (max-width: 768px) {
  .sidebar {
    width: 200px;
  }
  .content {
    margin-left: 200px;
  }
}

/* Mobile layout (max-width: 480px) */
@media only screen and (max-width: 480px) {
  .sidebar {
    width: 150px;
  }
  .content {
    margin-left: 200px;
  }
}

@media only screen and (max-width: 480px) {
  .sidebar-header {
    font-size: 10px;
    text-align: center;
  }
  .sidebar-header .logo {
    margin-bottom: 10px;
  }
  .sidebar-header .logo img {
    width: 10px;
  }
}

#sidebarToggle {
    position: fixed;
    top: 10px;
    left: 10px;
    z-index: 1;
    border: none;
    transition: transform 0.3s ease; /* Smooth rotation transition */
}

#sidebarToggle.rotate {
    transform: rotate(180deg); /* Rotate button 180 degrees */
}

/* Slideshow container */
.slideshow-container {
  max-width: 1000px;
  position: relative;
  margin: auto;
}

.mySlides {
  display: none;
  text-align: center;
}

/* Remove the fade animation */
.mySlides {
  animation: fade;
}

/* Fading animation */
.fade {
  animation-name: fade;
  animation-duration: 1.5s;
}

@keyframes fade {
  from {opacity: .4} 
  to {opacity: 1}
}

/* On smaller screens, decrease text size */
@media only screen and (max-width: 300px) {
  .text {font-size: 11px}
}

/* Media queries for responsiveness */
@media only screen and (max-width: 768px) {
  .slideshow-container {
    max-width: 400px; /* adjust the max-width to your liking */
  }
  .mySlides img {
    height: 200px; /* adjust the height to your liking */
  }
}

@media only screen and (max-width: 480px) {
  .slideshow-container {
    max-width: 200px; /* adjust the max-width to your liking */
  }
  .mySlides img {
    height: 150px; /* adjust the height to your liking */
    max-width: 160px;
  }
  #wc-text {
    font-size: 18px;
    margin-right: 15px;
  }
}

.text {
  color: #f2f2f2;
  font-size: 15px;
  padding: 8px 12px;
  position: absolute;
  bottom: 8px;
  width: 100%;
  text-align: center;
}

/* On smaller screens, decrease text size */
@media only screen and (max-width: 300px) {
  .prev, .next,.text {font-size: 11px}
} 

/* medium size of mobile phone */
@media only screen and (max-width: 425px) {
  .main {
    margin: 78px;
    overflow: hidden;
  }
}
</style>
<body>
<div id="toggle-btn">
        <button class="bg-transparent" style=" width: 40px;" id="sidebarToggle" type="button">
            <span><img src="../images/icons8-menu-48.png" alt="" style=" width:25px;"></span> <!-- You can use an icon or text -->
        </button>
    </div>
    <!-- Sidebar -->
    <div class="container">
      <div class="sidebar" id="sidebar">
        <div class="sidebar-header mt-4">
          <h3 style="font-size: 20px;">
            <img src="../images/icons8-tooth-50.png" alt=""style=" width: 30px;">
            <a id="dental-clinic-btn" href="#" style="text-decoration: none; color: #fff; ">Dental Clinic</a>
          </h3>
        </div>
        <ul class="list-unstyled components">
          <li class="active">
            <a id="home-btn" href="#homeSubmenu" data-bs-toggle="collapse" aria-expanded="false" class="dropdown-toggle">Patient Records  </a>
            <ul class="collapse list-unstyled bg-transparent" id="homeSubmenu">
              <li>
                <a href="#">Patient Info</a>
              </li>
              <li>
                <a href="#">Treatment Plan</a>
              </li>
              <li>
                <a href="#">Appointment</a>
              </li>
            </ul>
          </li>
          <li>
            <a href="#">Inventory</a>
          </li>
          <li>
            <a href="#">Billing</a>
          </li>
          <li>
            <a href="#">Treatment Plan</a>
          </li>
          <li>
            <a href="#">View</a>
          </li>
          <li>
            <a href="logout.php" style=" text-decoration: none; color: #fff;">Logout</a>
          </li>
        </ul>
      </div>
    </div>

</body>
</html>
