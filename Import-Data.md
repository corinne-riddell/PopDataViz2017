PopDataViz2017 Hackathon Datasets
---------------------------------

Please feel free to use your own data for the hackathon, or one of the
six described below. We have provided six datasets, three suitable for
beginners, and 3 suitable for more advanced users. They're organized
below by topic area. Some of these datasets are quite large, so we
recommend you only download the dataset you are interested in using. To
easily download your dataset of choice, first setup an RStudio Project:

1.  Open RStudio. Click: File &gt; New Project … &gt; Existing
    Directory &gt; Select the folder where you would like to store your
    project's data and its visualization.

2.  Once you create the project, RStudio will reopen a window specific
    to that project and its home directory. Type getwd() in the code
    console and notice the pathway points to your project folder.

3.  Read the descriptions below to decide which dataset you would like
    to use. Three of them are saved in the Github repository, and the
    other three are read in from an R package or from hard-coded data,
    included below.

4.  If necessary, download the dataset of choice from Github. They can
    be found in the /Data folder. Place it in the project folder
    you created.

5.  If you set up the project correctly, you can run the code for your
    chosen dataset to load it into R and you will not need to customize
    the pathway for the directory. Let us know if you run into any
    trouble!

Data descriptions
-----------------

**1. Canadian Emergency Room Wait Times (health - beginner)**

Wait times in Canada to receive emergency care have increased. These
data were released by the Canadian Institute for Health Information
(CIHI) and detail wait times by province, and age group, and stratified
by whether patients were admitted or not admitted. The data contains 32
rows and 10 variables.

Variables include:

-   `Province`: Province or territory for which data was provided.
-   `Age.group`: Five-year age groupings, and 65+
-   `Num.ED.visits`: The total number of emergency room visits for the
    province
-   `ED.LOS.90.less`: The 90th percentile of time for which people
    visiting the ED had to wait (i.e., 90% spent less than this amount
    of time)
-   `Not.admitted.num.visits`: The number of people not admitted to the
    ED room who made a visit.
-   `Not.admitted.percent.visits`: The percent of ED visits that were
    not admitted
-   `Not.admitted.LOS.90.less`: The 90th percentile of time for which
    people not admitted to the ED had to wait
-   `Admitted.num.visits`, `Admitted.percent.visits`,
    `Admitted.LOS.90.less`: same as the previous three items, but for
    people who were admitted to the emergency room.

If you would like to use this dataset, read in the data below. You can
easily do this by clicking any row of the code and then hitting
Command+Enter on a Mac or Ctrl+Enter on Windows/Linux:

    ed.wait.times <- data.frame(stringsAsFactors=FALSE,
                          Province = c("P.E.I.", "P.E.I.", "P.E.I.", "P.E.I.",
                                       "N.S.", "N.S.", "N.S.", "N.S.", "Ont.",
                                       "Ont.", "Ont.", "Ont.", "Man.", "Man.", "Man.",
                                       "Man.", "Sask.", "Sask.", "Sask.", "Sask.",
                                       "Alta.", "Alta.", "Alta.", "Alta.", "B.C.",
                                       "B.C.", "B.C.", "B.C.", "Y.T.", "Y.T.", "Y.T.",
                                       "Y.T."),
                         Age.group = c("0–4", "5–19", "20–64", "65+", "0–4",
                                       "5–19", "20–64", "65+", "0–4", "5–19",
                                       "20–64", "65+", "0–4", "5–19", "20–64", "65+",
                                       "0–4", "5–19", "20–64", "65+", "0–4", "5–19",
                                       "20–64", "65+", "0–4", "5–19", "20–64", "65+",
                                       "0–4", "5–19", "20–64", "65+"),
                     Num.ED.visits = c(1806, 3373, 12678, 6000, 25513, 43033,
                                       173434, 71933, 492683, 864528, 3515312,
                                       1439203, 30444, 45839, 186421, 66228, 26989,
                                       39294, 170091, 56635, 219355, 348416, 1317309,
                                       390146, 106875, 187197, 911543, 382119, 2852,
                                       5337, 24930, 5353),
                    ED.LOS.90.less = c(5.4, 6.5, 7.7, 16.5, 4.7, 5.5, 8, 16.4, 4.8,
                                       5.2, 7.3, 16.2, 5.7, 7.4, 11.5, 27.2, 5.5,
                                       6.7, 10.4, 21.8, 4.5, 4.9, 7.4, 13, 4.9, 5.4,
                                       7.9, 20, 2.9, 3.3, 4.4, 8.8),
           Not.admitted.num.visits = c(1647, 3213, 11872, 4858, 24302, 41510,
                                       164021, 59907, 471244, 830574, 3275128,
                                       1116109, 28542, 43390, 172725, 50295, 24605,
                                       36071, 148719, 36871, 211404, 337869, 1229783,
                                       309611, 101695, 178052, 828053, 276927, 2780,
                                       5223, 23781, 4571),
       Not.admitted.percent.visits = c(91.2, 95.3, 93.6, 81, 95.3, 96.5, 94.6,
                                       83.3, 95.6, 96.1, 93.2, 77.6, 93.8, 94.7,
                                       92.7, 75.9, 91.2, 91.8, 87.4, 65.1, 96.4, 97,
                                       93.4, 79.4, 95.2, 95.1, 90.8, 72.5, 97.5, 97.9,
                                       95.4, 85.4),
          Not.admitted.LOS.90.less = c(5.3, 6.2, 6.6, 7.5, 4.5, 5.3, 7.1, 9.6, 4.4,
                                       4.8, 6.1, 7.7, 4.9, 6.6, 9.3, 16.8, 4.9, 6,
                                       7.7, 9.1, 4.2, 4.5, 6.2, 7.5, 4.5, 4.8, 6,
                                       7.2, 2.7, 3.1, 3.7, 4.3),
               Admitted.num.visits = c(159, 160, 806, 1142, 1211, 1523, 9413,
                                       12026, 21439, 33954, 240184, 323094, 1902,
                                       2449, 13696, 15933, 2384, 3223, 21372, 19764,
                                       7951, 10547, 87526, 80535, 5180, 9145, 83490,
                                       105192, 72, 114, 1149, 782),
           Admitted.percent.visits = c(8.8, 4.7, 6.4, 19, 4.7, 3.5, 5.4, 16.7, 4.4,
                                       3.9, 6.8, 22.4, 6.2, 5.3, 7.3, 24.1, 8.8,
                                       8.2, 12.6, 34.9, 3.6, 3, 6.6, 20.6, 4.8, 4.9,
                                       9.2, 27.5, 2.5, 2.1, 4.6, 14.6),
              Admitted.LOS.90.less = c(6.2, 20.7, 47.3, 46, 7.3, 10.1, 29.8, 40,
                                       11.6, 18.2, 29.5, 34.8, 15, 20.1, 38.7,
                                       49.8, 9.9, 16.8, 31.4, 35, 11.9, 20.4, 27.9, 30.3,
                                       10.9, 23.1, 44.8, 43.3, 27.7, 18.7, 26.2,
                                       25.7)
    )

Data downloaded from
<https://www.cihi.ca/en/emergency-department-wait-times-in-canada-continuing-to-rise>.
This link downloads a spreadsheet. The data we are using for this
project is from the 5th sheet. Feel free to see the other pages in the
sheet for more information/data you might like to use.

**2. US Hospital Charges (health - advanced)**

There is significant variation across hospitals in what is charged for
common services. This dataset provides charge data for the 100 most
common inpatient services and 30 most common outpatient services for a
set of hospitals in the United States. The data contain 163,065 rows and
12 columns.

Variables included in this dataset:

-   `DRG.Definition`: aka the "Diagnosis Related Group" definition. The
    classification groups similar clinical conditions and procedures.
    For example, 522 is the DRG code for major back problems without
    major complication or comorbidity. The description of the DRG
    category is provided beside the code, as part of this variable.

Hospital Variables:

-   `Provider.Id`: an identifier for the hospital.
-   `Provider.Name`
-   `Provider.Street.Address`
-   `Provider.City`
-   `Provider.State`
-   `Provider.Zip.Code`
-   `Hospital.Referral.Region..HRR..Description`

Charge Information:

-   `Total.Discharges`: The number of discharges billed by the provider
    for inpatient hospital services.

-   `Average.Covered.Charges`: The provider's average charge for
    services covered by Medicare for all discharges in this DRG. This
    varies across hospitals because of differences in hospital
    charge structures.

-   `Average.Total.Payments`: The average total payments to all
    providers for the MS-DRG including the MS-DRG amount, teaching,
    disproportionate share, capital, and outlier payments for all cases.
    Also included in average total payments are co-payment and
    deductible amounts that the patient is responsible for and any
    additional payments by third parties for coordination of benefits.

-   `Average.Medicare.Payments`: The average amount that Medicare pays
    to the provider for Medicare's share of the MS-DRG. Average Medicare
    payment amounts include the MS-DRG amount, teaching,
    disproportionate share, capital, and outlier payments for all cases.
    Medicare payments DO NOT include beneficiary co-payments and
    deductible amounts nor any additional payments from third parties
    for coordination of benefits. Note: In general, Medicare FFS claims
    with dates-of-service or dates-of-discharge on or after April 1,
    2013, incurred a 2 percent reduction in Medicare payment. This is in
    response to mandatory across-the-board reductions in Federal
    spending, also known as sequestration.

If you would like to use this dataset, read in the line below:

    ffs <- read.csv("./Data/Medicare_Provider_Charge_Inpatient_DRG100_FY2011.csv")

-   Data downloaded from
    <https://www.cms.gov/Research-Statistics-Data-and-Systems/Statistics-Trends-and-Reports/Medicare-Provider-Charge-Data/Inpatient2011.html>.

-   Variable descriptions from
    <https://data.cms.gov/api/views/97k6-zzx3/files/4496fc4f-5f10-43e4-8183-b6da867f8981?download=true&filename=Medicare_Hospital_Inpatient_PUF_Methodology_2017-08-30.pdf>.

Download from
<https://data.worldbank.org/data-catalog/world-development-report-2014>.
The dataset found on this website downloads a spreadsheet. The data we
are using for this project is from the first sheet.

**3. Life expectancy at birth, 1950-2015, by country
(demography/sociology - beginner)**

These data come from the World Population Prospects, 2015 revision. The
datasets (one for males, one for females) contain the life expectancy at
birth, by country, and specified world regions, from 1950 to 2015 for
every five-year period of time. These datasets are included as part of
the `wpp2015` package that you can install to gain access. Each dataset
conains 241 rows and 16 columns.

To use these data, run the following lines of code:

    install.packages("wpp2015")
    library(wpp2015)

    data(e0M) #this loads the dataset "e0M" into memory. It is for males.
    data(e0F) #ditto, for females

You may want to use the data as is, or add in other country or regional
characteristics from the internet to enrich your dataset. This is not
required, it all depends on what you hope to visualize! If you find
other information you'd like to add in, we can help you merge it to
these data if you need advice.

**4. Police traffic stop data for Vermont and Florida,
(demography/sociology - advanced)**

These datasets came from the Stanford Policing Project. They contain
every traffic stop conducted by a police officer in the state of Vermont
between 2010 and 2015 and the state of Florida between 2010 and October
2016. There is one row per traffic stop. Depending on what you would
like to visualize, you may want to aggregate these data by time, space,
or a clustering variable before visualization. Let us know if we can
help you with pre-processing your data. The Vermont dataset contains
283,285 rows and 23 columns, while the Florida dataset contains
5,421,446 rows and 28 columns

Variables included:

-   `id`: An identifier for the stop.
-   `state`: The state abbreviation. -`stop_date`: In the format
    YYYY-MM-DD, denoting the date the stop was conducted.
-   `stop_time`: Time of the stop in 24-hr format.
-   `location_raw`: The location of the stop, as recorded by the state..
-   `county_name`: The county where the stop took place.
-   `count_fips`: A numeric ID for the county.
-   `fine_grained_location`: Inconsistenly coded and formatted, but more
    granular detail about the stop location.
-   `police department`: The policy department of the officer who
    conducted the stop.
-   `driver_age_raw`: The driver's age as coded in Florida (Florida
    only; no data in Vermont on age).
-   `driver_age`: The driver's age as recoded by the Stanford
    Policing Project. (No data in Vermont on age)
-   `driver_gender`: The gender of the driver.
-   `drivre_race_raw`: Race as coded by the state.
-   `drivre_race`: Race as recoded by the Stanford Policing Project.
-   `violation_raw`: The violation as coded by the state.
-   `violation`: The violation as coded by the Stanford Policing Project
    (to make consistent across states).
-   `search_conducted`: TRUE/FALSE indicator for whether the car
    was searched.
-   `search_type_raw`: Search variable originally provided by the state.
-   `contraband_found`: Indicator for whether the search
    yielded contraband. (No data from Florida)
-   `stop_outcome`: Categorical indicator for whether the stopped
    individual was given a warning, a citation, or was arrested.
-   `is_arrested`: TRUE/FALSE indicator for whether an arrest was made.
-   `officer_id`: Identifier variable to cluster stops for each officer.
-   Additional officer characteristics coded for Florida:
    `officer_gender`, `officer_age`, `officer_race`, `officer_rank`
-   `out_of_state`: Whether the driver was from out of state.

To use these data, run the following lines of code. You can use either
dataset, or both, depending on what you'd like to visualize:

    VT.data <- gzfile("./Data/VT-clean.csv.gz")
    VT.stops <- read.csv(VT.data, stringsAsFactors=FALSE, header=T, nrows=1300000) #takes 20 seconds

    FL.data <- readRDS("./Data/FL_clean.rds")

-   Data downloaded from <https://openpolicing.stanford.edu/data/>, see
    the download link for Vermont.

**5. Worldwide Key Development Indicators, 2012 (Economics - beginner)**

This dataset contains key development indicators by country, as
collected by the World Bank. The data contain 133 rows and 13 columns.

Variables include:

-   `Country`: Country name
-   `Pop.millions`: Population of the country, in millions, 2012.
-   `Pop.annual.growth`: Average annual growth (%) from 2000--2012.
-   `Density.per.sq.km`: Density of people per square kilometre, 2012
-   `Percent.0.14`: Percent of the population between 0 and 14 years of
    age, 2012
-   `GNI`: Gross National Income, 2012.
-   `GNI.per.capita`: GNI per capita, 2012.
-   `PPP`: National purchasing power parity, 2012.
-   `PPP.per.capita`: PPP per capital, 2012.
-   `GDP.per.capita`: Gross domestic product per capita, 2012.
-   `LE.birth.males`: Life expectancy at birth for males in 2011.
-   `LE.birth.females`: Life expectancy at birth for females in 2011
-   `Adult.literacy.rate`: Percentage of adults (15 years or older) who
    can read, 2005-2011.

If you would like to use this dataset, read in the data below. You can
easily do this by clicking any row of the code and then hitting
Command+Enter on a Mac or Ctrl+Enter on Windows/Linux:

    world.dev <- data.frame(stringsAsFactors=FALSE,
                   Country = c("Afghanistan", "Albania", "Algeria", "Angola",
                               "Argentina", "Armenia", "Australia", "Austria",
                               "Azerbaijan", "Bangladesh", "Belarus", "Belgium", "Benin",
                               "Bolivia", "Bosnia and Herzegovina", "Brazil",
                               "Bulgaria", "Burkina Faso", "Burundi", "Cambodia",
                               "Cameroon", "Canada", "Central African Republic", "Chad",
                               "Chile", "China", "Hong Kong SAR, China", "Colombia",
                               "Congo, Dem. Rep.", "Congo, Rep.", "Costa Rica",
                               "Cote d\'Ivoire", "Croatia", "Czech Republic", "Denmark",
                               "Dominican Republic", "Ecuador", "Egypt, Arab Rep.",
                               "El Salvador", "Eritrea", "Ethiopia", "Finland", "France",
                               "Georgia", "Germany", "Ghana", "Greece", "Guatemala",
                               "Guinea", "Haiti", "Honduras", "Hungary", "India",
                               "Indonesia", "Iran, Islamic Rep.", "Iraq", "Ireland",
                               "Israel", "Italy", "Japan", "Jordan", "Kazakhstan",
                               "Kenya", "Korea, Rep.", "Kyrgyz Republic", "Lao PDR",
                               "Lebanon", "Liberia", "Libya", "Lithuania", "Madagascar",
                               "Malawi", "Malaysia", "Mali", "Mauritania", "Mexico",
                               "Moldova", "Morocco", "Mozambique", "Myanmar", "Nepal",
                               "Netherlands", "New Zealand", "Nicaragua", "Niger",
                               "Nigeria", "Norway", "Pakistan", "Panama",
                               "Papua New Guinea", "Paraguay", "Peru", "Philippines", "Poland",
                               "Portugal", "Romania", "Russian Federation", "Rwanda",
                               "Saudi Arabia", "Senegal", "Serbia", "Sierra Leone",
                               "Singapore", "Slovak Republic", "Somalia",
                               "South Africa", "South Sudan", "Spain", "Sri Lanka", "Sudan",
                               "Sweden", "Switzerland", "Syrian Arab Republic",
                               "Tajikistan", "Tanzania", "Thailand", "Togo", "Tunisia",
                               "Turkey", "Turkmenistan", "Uganda", "Ukraine",
                               "United Arab Emirates", "United Kingdom", "United States", "Uruguay",
                               "Uzbekistan", "Venezuela, RB", "Vietnam",
                               "West Bank and Gaza", "Yemen, Rep.", "Zambia", "Zimbabwe"),
              Pop.millions = c(30, 3, 38, 21, 41, 3, 23, 8, 9, 155, 9, 11, 10, 10,
                               4, 199, 7, 16, 10, 15, 22, 35, 5, 12, 17, 1351, 7,
                               48, 66, 4, 5, 20, 4, 11, 6, 10, 15, 81, 6, 6, 92, 5,
                               66, 5, 82, 25, 11, 15, 11, 10, 8, 10, 1237, 247, 76, 33,
                               5, 8, 61, 128, 6, 17, 43, 50, 6, 7, 4, 4, 6, 3, 22,
                               16, 29, 15, 4, 121, 4, 33, 25, 53, 27, 17, 4, 6, 17,
                               169, 5, 179, 4, 7, 7, 30, 97, 39, 11, 21, 144, 11, 28,
                               14, 7, 6, 5, 5, 10, 51, 11, 46, 20, 37, 10, 8, 22, 8,
                               48, 67, 7, 11, 74, 5, 36, 46, 9, 63, 314, 3, 30, 30,
                               89, 4, 24, 14, 14),
         Pop.annual.growth = c(3.1, -0.4, 1.6, 3.4, 0.9, -0.3, 1.4, 0.5, 1.2, 1.3,
                               -0.5, 0.7, 3.1, 1.8, 0, 1.1, -0.9, 2.9, 3.2, 1.6,
                               2.6, 1, 1.8, 3.4, 1, 0.6, 0.6, 1.5, 2.8, 2.7, 1.7, 1.7,
                               -0.3, 0.2, 0.4, 1.4, 1.8, 1.7, 0.5, 3.7, 2.7, 0.4,
                               0.6, 0.2, 0, 2.5, 0.3, 2.5, 2.2, 1.4, 2, -0.2, 1.4, 1.4,
                               1.2, 2.6, 1.6, 1.9, 0.6, 0, 2.3, 1, 2.7, 0.5, 1.1,
                               1.7, 2.6, 3.1, 1.4, -1.3, 2.9, 2.8, 1.8, 3.1, 2.8, 1.3,
                               -0.2, 1, 2.7, 0.7, 1.4, 0.4, 1.2, 1.3, 3.7, 2.6, 0.9,
                               1.8, 1.8, 2.4, 1.9, 1.2, 1.8, 0, 0.2, -0.4, -0.2, 2.6,
                               2.8, 2.8, -0.3, 3.1, 2.3, 0, 2.7, 1.3, 4.1, 1.1, 0.5,
                               2.4, 0.6, 0.9, 2.6, 2.2, 2.8, 0.6, 2.6, 1, 1.3, 1.2,
                               3.4, -0.6, 9.3, 0.6, 0.9, 0.2, 1.6, 1.7, 1.1, 2.7, 2.6,
                               2.8, 0.8),
         Density.per.sq.km = c("46", "115", "16", "17", "15", "104", "3", "103",
                               "112", "1,188", "47", "368", "89", "10", "75", "23",
                               "67", "60", "384", "84", "46", "4", "7", "10", "23",
                               "145", "6,866", "43", "29", "13", "94", "62", "76",
                               "136", "132", "213", "62", "81", "304", "61", "92",
                               "18", "120", "65", "235", "111", "88", "141", "47", "369",
                               "71", "110", "416", "136", "47", "75", "67", "365",
                               "207", "350", "71", "6", "76", "515", "29", "29",
                               "433", "44", "3", "48", "38", "169", "89", "12", "4", "62",
                               "108", "73", "32", "81", "192", "497", "17", "50",
                               "14", "185", "16", "232", "51", "16", "17", "23", "324",
                               "127", "115", "93", "9", "464", "13", "71", "83",
                               "83", "7,589", "113", "16", "42", NA, "93", "324",
                               "16", "23", "200", "122", "57", "54", "131", "122", "69",
                               "96", "11", "182", "79", "110", "261", "34", "19",
                               "70", "34", "286", "672", "45", "19", "35"),
              Percent.0.14 = c(47L, 21L, 27L, 48L, 24L, 20L, 19L, 15L, 22L, 31L,
                               15L, 17L, 43L, 35L, 16L, 25L, 14L, 46L, 44L, 31L,
                               43L, 16L, 40L, 49L, 21L, 18L, 12L, 28L, 45L, 42L, 24L,
                               41L, 15L, 15L, 18L, 31L, 30L, 31L, 31L, 43L, 43L, 16L,
                               18L, 18L, 13L, 39L, 15L, 41L, 42L, 35L, 36L, 15L, 29L,
                               29L, 24L, 41L, 22L, 28L, 14L, 13L, 34L, 25L, 42L,
                               15L, 30L, 36L, 22L, 43L, 29L, 15L, 43L, 45L, 27L, 47L,
                               40L, 29L, 17L, 28L, 45L, 25L, 36L, 17L, 20L, 33L, 50L,
                               44L, 19L, 34L, 29L, 38L, 33L, 29L, 35L, 15L, 15L, 15L,
                               15L, 44L, 30L, 44L, 16L, 42L, 16L, 15L, 47L, 30L, 42L,
                               15L, 25L, 41L, 17L, 15L, 35L, 36L, 45L, 18L, 42L,
                               23L, 26L, 29L, 49L, 14L, 14L, 18L, 20L, 22L, 29L, 29L,
                               23L, 41L, 41L, 47L, 40L),
                       GNI = c("16.6", "12.9", "155.1", "95.4", NA, "11.1", "1,
                              351.2", "407.6", "56.3", "129.2", "61.8", "501.3",
                               "7.5", "23.3", "17.8", "2,311.1", "50.2", "10.9", "2.4",
                               "13.0", "25.4", "1,777.9", "2.2", "9.3", "249.5", "7,
                              748.9", "261.6", "333.6", "14.8", "11.1", "42.0",
                               "24.2", "56.7", "190.6", "334.1", "56.2", "80.5", "241.8",
                               "22.5", "2.8", "37.4", "254.1", "2,742.9", "14.8",
                               "3,603.9", "39.3", "262.4", "47.0", "5.3", "7.7",
                               "16.4", "123.2", "1,890.4", "844.0", NA, "191.2", "178.8",
                               "224.7", "2,061.3", "6,105.8", "29.9", "163.5",
                               "36.2", "1,133.8", "5.5", "8.4", "40.7", "1.6", NA,
                               "41.3", "9.7", "5.0", "286.4", "9.8", "4.2", "1,176.9",
                               "7.4", "97.1", "12.8", NA, "19.2", "809.1", "134.9",
                               "9.9", "6.4", "241.1", "496.2", "225.4", "37.7", "12.8",
                               "22.0", "176.5", "238.7", "488.3", "216.6", "179.6",
                               "1,822.7", "6.2", "500.5", "14.2", "38.1", "3.5",
                               "250.8", "92.9", NA, "389.8", "7.0", "1,391.4", "59.3",
                               "53.8", "535.0", "661.6", "56.3", "6.9", "26.7",
                               "347.9", "3.3", "44.8", "801.1", "28.7", "16.0", "159.6",
                               "321.7", "2,418.5", "15,734.6", "45.9", "51.3",
                               "373.5", "124.1", NA, "26.0", "19.1", "9.3"),
            GNI.per.capita = c("570", "4,090", "4,110", "4,580", NA, "3,720",
                               "59,570", "48,160", "6,050", "840", "6,530", "44,
                              990", "750", "2,220", "4,650", "11,630", "6,870", "670",
                               "240", "880", "1,170", "50,970", "490", "740", "14,
                              280", "5,740", "36,560", "6,990", "220", "2,550", "8,
                              740", "1,220", "13,290", "18,130", "59,770", "5,470", "5,
                              190", "3,000", "3,580", "450", "410", "46,940", "41,
                              750", "3,280", "44,010", "1,550", "23,260", "3,120",
                               "460", "760", "2,070", "12,390", "1,530", "3,420", NA,
                               "5,870", "38,970", "28,930", "33,840", "47,870", "4,
                              720", "9,730", "840", "22,670", "990", "1,260", "9,190",
                               "370", NA, "13,850", "430", "320", "9,800", "660",
                               "1,110", "9,740", "2,070", "2,940", "510", NA, "700",
                               "48,250", "30,620", "1,650", "370", "1,430", "98,
                              860", "1,260", "9,910", "1,790", "3,290", "5,880", "2,
                              470", "12,670", "20,580", "8,420", "12,700", "560", "18,
                              030", "1,040", "5,280", "580", "47,210", "17,170", NA,
                               "7,610", "650", "30,110", "2,920", "1,450", "56,210",
                               "82,730", "2,610", "860", "570", "5,210", "500", "4,
                              150", "10,830", "5,550", "440", "3,500", "36,040", "38,
                              250", "50,120", "13,510", "1,720", "12,470", "1,400",
                               NA, "1,110", "1,350", "680"),
                       PPP = c("40.7", "29.7", "285.0", "114.3", NA, "20.8",
                               "982.2", "373.2", "87.5", "319.9", "143.9", "447.6",
                               "15.8", "52.1", "36.0", "2,328.8", "112.4", "24.9",
                               "5.5", "35.1", "50.3", "1,483.6", "3.9", "16.4",
                               "372.1", "12,435.4", "379.6", "482.2", "24.5", "15.2",
                               "60.5", "38.8", "84.3", "259.8", "242.3", "101.0", "148.5",
                               "536.3", "42.8", "3.4", "104.2", "209.2", "2,412.6",
                               "26.4", "3,430.1", "49.2", "287.2", "74.8", "11.3",
                               "12.6", "30.9", "205.9", "4,749.2", "1,188.0", NA,
                               "140.2", "164.6", "218.0", "2,002.3", "4,629.7", "38.8",
                               "200.7", "76.1", "1,548.7", "12.6", "18.1", "63.7",
                               "2.5", NA, "67.9", "21.2", "13.9", "483.2", "17.2",
                               "9.6", "2,015.8", "13.1", "166.6", "25.7", NA, "41.1",
                               "731.5", "132.0", "23.7", "11.2", "409.1", "336.1",
                               "543.6", "67.8", "19.9", "37.5", "306.9", "425.2",
                               "816.0", "260.7", "347.8", "3,260.6", "13.9", "694.4",
                               "26.3", "80.8", "8.1", "324.6", "134.0", NA, "572.6",
                               NA, "1,493.8", "124.5", "75.3", "420.1", "449.8",
                               "116.5", "17.8", "73.6", "630.0", "6.1", "100.9", "1,
                              345.7", "49.9", "41.4", "332.5", "378.3", "2,331.9", "15,
                              887.6", "52.9", "111.6", "393.0", "305.6", NA,
                               "53.7", "22.8", NA),
            PPP.per.capita = c("1,400", "9,390", "7,550", "5,490", NA, "6,990",
                               "43,300", "44,100", "9,410", "2,070", "15,210", "40,
                              170", "1,570", "4,960", "9,380", "11,720", "15,390",
                               "1,510", "560", "2,360", "2,320", "42,530", "860", "1,
                              320", "21,310", "9,210", "53,050", "10,110", "370", "3,
                              510", "12,590", "1,960", "19,760", "24,710", "43,340",
                               "9,820", "9,590", "6,640", "6,790", "560", "1,140",
                               "38,630", "36,720", "5,860", "41,890", "1,940", "25,
                              460", "4,960", "980", "1,240", "3,890", "20,710", "3,
                              840", "4,810", NA, "4,300", "35,870", "28,070", "32,
                              870", "36,290", "6,130", "11,950", "1,760", "30,970", "2,
                              260", "2,730", "14,400", "600", NA, "22,760", "950",
                               "880", "16,530", "1,160", "2,520", "16,680", "3,690",
                               "5,040", "1,020", NA, "1,500", "43,620", "29,960",
                               "3,960", "650", "2,420", "66,960", "3,030", "17,830",
                               "2,780", "5,610", "10,240", "4,400", "21,170", "24,
                              770", "16,310", "22,720", "1,250", "25,010", "1,920", "11,
                              180", "1,360", "61,100", "24,770", NA, "11,190",
                               NA, "32,320", "6,120", "2,030", "44,150", "56,240", "5,
                              200", "2,220", "1,590", "9,430", "920", "9,360", "18,
                              190", "9,640", "1,140", "7,290", "42,380", "36,880",
                               "50,610", "15,570", "3,750", "13,120", "3,440", NA,
                               "2,310", "1,620", NA),
            GDP.per.capita = c("4.4", "0.5", "0.6", "3.5", NA, "7.0", "1.8",
                               "0.4", "3.1", "5.1", "1.6", "-1.1", "2.6", "3.5",
                               "-0.6", "0.0", "1.4", "6.9", "0.7", "5.4", "2.1", "0.6",
                               "2.1", "1.9", "4.6", "7.3", "0.3", "2.6", "4.3",
                               "1.1", "3.6", "7.0", "-1.7", "-1.5", "-0.8", "2.6", "3.3",
                               "0.5", "1.0", "3.6", "5.7", "-0.7", "-0.5", "5.3",
                               "0.6", "5.6", "-6.2", "0.4", "1.3", "1.4", "1.4",
                               "-1.4", "1.9", "4.9", NA, "5.7", "0.7", "2.8", "-2.7",
                               "2.1", "0.6", "3.5", "1.5", "1.6", "-2.1", "6.1", "0.4",
                               "7.9", NA, "5.3", "0.3", "-1.0", "3.9", "-4.1",
                               "4.9", "2.6", "-0.8", "1.2", "4.7", NA, "3.4", "-1.4",
                               "2.3", "3.7", "7.0", "3.6", "1.7", "2.4", "8.9", "5.7",
                               "-2.9", "5.0", "4.8", "1.9", "-3.0", "4.0", "3.0",
                               "5.0", "4.8", "0.7", "-1.2", "13.0", "-1.1", "1.8",
                               NA, "1.3", "-57.7", "-1.5", "9.2", "0.6", "0.0", "-0.1",
                               "0.8", "5.4", "3.7", "6.1", "2.9", "2.6", "0.9",
                               "9.7", "0.0", "0.4", "-0.8", "-0.5", "1.5", "3.6", "6.6",
                               "3.9", "3.9", NA, "-2.2", "4.0", "2.2"),
            LE.birth.males = c("49", "74", "72", "50", "72", "71", "80", "78",
                               "68", "68", "65", "78", "54", "64", "73", "70",
                               "71", "54", "49", "62", "51", "79", "47", "48", "76",
                               "72", "80", "70", "47", "56", "77", "54", "74", "75",
                               "78", "71", "73", "71", "67", "59", "58", "77", "78",
                               "70", "78", "63", "79", "68", "53", "61", "71", "71",
                               "64", "68", "71", "66", "78", "80", "80", "79", "72",
                               "64", "56", "78", "66", "66", "70", "56", "72", "68",
                               "65", "54", "72", "50", "57", "75", "66", "70", "49",
                               "63", "68", "79", "79", "71", "54", "51", "79", "65",
                               "74", "61", "70", "71", "66", "73", "78", "71", "63",
                               "54", "73", "58", "72", "47", "80", "72", "50", "52",
                               NA, "79", "72", "60", "80", "81", "74", "64", "57",
                               "71", "56", "73", "72", "61", "53", "66", "76", "79",
                               "76", "73", "65", "71", "73", "71", "64", "49", "52"),
          LE.birth.females = c("49", "80", "75", "53", "80", "77", "84", "84",
                               "74", "70", "77", "83", "58", "69", "78", "77",
                               "78", "56", "52", "64", "53", "83", "50", "51", "82",
                               "75", "87", "77", "50", "59", "82", "57", "80", "81",
                               "82", "76", "79", "75", "77", "64", "61", "84", "85",
                               "77", "83", "65", "83", "75", "56", "63", "75", "79",
                               "67", "71", "75", "72", "83", "84", "85", "86", "75",
                               "74", "58", "84", "74", "69", "75", "58", "78", "79",
                               "68", "54", "77", "52", "60", "79", "73", "74", "51",
                               "67", "70", "83", "83", "77", "55", "53", "84", "66",
                               "79", "65", "75", "77", "72", "81", "84", "78", "75",
                               "57", "75", "60", "77", "48", "84", "80", "53", "53",
                               NA, "85", "78", "63", "84", "85", "77", "71", "59",
                               "78", "59", "77", "76", "69", "55", "76", "78", "83",
                               "81", "80", "71", "77", "77", "75", "67", "49", "50"),
       Adult.literacy.rate = c(NA, "96", "73", "70", "98", "100", NA, NA,
                               "100", "57", "100", NA, "42", "91", "98", "90",
                               "98", "29", "67", "74", "71", NA, "56", "34", "99",
                               "94", NA, "93", "67", NA, "96", "56", "99", NA,
                               NA, "90", "92", "72", "84", "68", "39", NA, NA,
                               "100", NA, "67", "97", "75", "41", "49", "85", "99",
                               "63", "93", "85", "78", NA, NA, "99", NA, "93",
                               "100", "87", NA, "99", "73", "90", "61", "89", "100",
                               "64", "75", "93", "31", "58", "93", "99", "56", "56",
                               "92", "60", NA, NA, "78", "29", "61", NA, "55",
                               "94", "61", "94", "90", "95", "100", "95", "98",
                               "100", "71", "87", "50", "98", "42", "96", NA, NA,
                               "89", NA, "98", "91", "71", NA, NA, "83", "100",
                               "73", "94", "57", "78", "91", "100", "73", "100", "90",
                               NA, NA, "98", "99", "96", "93", "95", "64", "71",
                               "92")
    )

**6. Occupational wages around the world, 1983-2008 (Economics -
advanced)** These data were originally derived from the the inquiry
database of the International Labour Organization (ILO). The data is
calibrated into a normalized wage rate for each occupation, either
hourly or monthly, for adult workers. The data contain 125,018 rows and
37 columns.

Variables included:

-   `y0`: year
-   `y2`: two digit country code
-   `y3`: three digit country code
-   `y4`: occupation code (from the ILO). See
    <http://www.ilo.org/public/english/bureau/stat/isco/docs/resol08.pdf>
    or
    <https://en.wikipedia.org/wiki/International_Standard_Classification_of_Occupations>
    to learn more about the occupational code mapping.

Variables starting with `h` are hourly wage variables, with varying
levels of calibration:

-   `hw1`: hourly: standard data LCU
-   `hw2wu`: hourly: country-specific calibration (uni) LCU
-   `hw3wu`: hourly: country-specific calibration with imputation (uni)
    LCU
-   `hw4wu`: hourly: uniform calibration (uni) LCU
-   `hw2wl`: hourly: country-specific calibration (lex) LCU
-   `hw3wl`: hourly: country-specific calibration with imputation (lex)
    LCU
-   `hw4wl`: hourly: uniform calibration (lex) LCU
-   `hw1us`: hourly: standard data US$
-   `hw2wuus`: hourly: country-specific calibration (uni) US$
-   `hw3wuus`: hourly: country-specific calibration with
    imputation (uni) US$
-   `hw4wuus`: hourly: uniform calibration (uni) US$
-   `hw2wlus`: hourly: country-specific calibration (lex) US$
-   `hw3wlus`: hourly: country-specific calibration with
    imputation (lex) US$
-   `hw4wlus`: hourly: uniform calibration (lex) US$

Variables starting with `m` are monthly, and in a similar format as the
hourly variables:

-   `mw1`: monthly: standard data LCU
-   `mw2wu`: monthly: country-specific calibration (uni) LCU
-   `hw3wu`: monthly: country-specific calibration with imputation (uni)
    LCU
-   `mw4wu`: monthly: uniform calibration (uni) LCU
-   `mw2wl`: monthly: country-specific calibration (lex) LCU
-   `mw3wl`: monthly: country-specific calibration with imputation (lex)
    LCU
-   `mw4wl`: monthly: uniform calibration (lex) LCU
-   `mw1us`: monthly: standard data US$
-   `mw2wuus`: monthly: country-specific calibration (uni) US$
-   `mw3wuus`: monthly: country-specific calibration with
    imputation (uni) US$
-   `mw4wuus`: monthly: uniform calibration (uni) US$
-   `mw2wlus`: monthly: country-specific calibration (lex) US$
-   `mw3wlus`: monthly: country-specific calibration with
    imputation (lex) US$
-   `mw4wlus`: monthly: uniform calibration (lex) US$

Remaining variables:

-   `currency`: currency as reported in ILO October Inquiry
-   `exrt`: exchange rate: LCU per US$
-   `conv`: conversion factor for wages in LCU
-   `curr_conv`: currency used for conversion factor

If you would like to use this dataset, read in the line below:

    install.packages("foreign") #this package helps us read data from other sources, like Stata.
    library(foreign)

    world.wages <- read.dta("./Data/oww3.dta")

-   More information about these data
    <http://www.ilo.org/wcmsp5/groups/public/---dgreports/---stat/documents/publication/wcms_087900.pdf>.
-   Data downloaded from <http://www.nber.org/oww/>, and originally
    derived from the International Labour Organization.
