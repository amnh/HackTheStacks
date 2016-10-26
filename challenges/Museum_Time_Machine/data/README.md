## AMNH Permanent Halls Master List with Variant Names
> ### 2016 March 29

Original data taken from in Valerie Thaler's spread sheet of Hall
names found in AMNH publications. More information about this data set
can be found at:
http://images.library.amnh.org/hiddencollections/resources/amnh-permanent-halls/

### History

The AMNH Library received funding from the Council on Library and
Information Resources' (CLIR) Hidden Collection grant (2012) to create
in-depth finding aids for expeditionary archives collections. The
project also resulted in brief histories of these expeditions and
biographies of those who participated in them to provide contextual
information to support the finding aids and to provide general
information. The data for the contextual records are encoded in the
metadata standard: Encoded Archival Context -- Corporate Bodies,
Persons and Families (EAC-CPF). The project team chose to use EAC-CPF
in order to reconnect collections held in different AMNH Departments
(effectively collocating materials that originated from the same
expedition), to reduce redundant work by utilizing the
biographical/historical notes from one source for finding aids, and to
increase resource discovery by leveraging linked data.

Though the project focused on persons and expeditions for EAC-CPF
description, we were able to set up additional entity lists for AMNH
Departments, Temporary Exhibits and Permanent Halls. Thanks to the
help of past volunteers (namely, Valerie Thaler for Permanent Halls
and Blosson Gerenter for Temporary Exhibits), the Project Metadata
Analyst (Iris Lee) reconfigured the data sets to map to EAC data
fields. Our current volunteers, Dale Dancis and Roxanne Edwards, are
adding descriptive, cited summaries and related persons, institutions
and departments to the Temporary Exhibits data set. Iris has edited
the format of Valerie's original Permanent Halls spreadsheet and added
controlled names for each hall.

### What's In This Spreadsheet

The CSV labeled "PH_all_floors" consists of data for 103 halls,
including variant names used in AMNH's General Guides, Official
Guides, and other AMNH publications. Also included are dates of use
for the variant names, the floor and section for which the hall was or
is currently located, a status of the hall (such as "historic" or
"current"), a controlled name for each hall to promote consistency and
interoperability with other Departments, a unique identifier for each
hall, and a notes field that contains information about the
construction, opening, or contents of the hall.

### Note About Physical Location Within the Museum

Google maps has assigned latitute and longitude values to individual
halls. It may be possible to map a geographic location to each hall in
cpfDescription > description > place > placeEntry. Should this be
available at the time of ingest into xEAC, Columns G, H, I, and J can
be concatenated into a sentence for a descriptiveNote under
placeEntry. Example: [Hall name] location on Floor [1], Section
[1]. This may be harder for halls that have moved over time. Need to
review options here.

_Suggestions_

Use Data > Filter to isolate a section of data to search
Filter can also perform keyword searches on a single column
Sort data according to need (currently sorted alphabetically by Control name, source, floor)"

---

### Index of Data Fields

    COLUMN A = Record identifier (unique id)
    COLUMN B = Status of the hall (current, moved, historic, reconstructed)
    COLUMN C = Control name (assigned by Iris with Diana Shih's consultation)
    COLUMN D = Short name (for reference)
    COLUMN E = Names used in AMNH publications (variant names found in General Guides and other AMNH publications)
    COLUMN F = Use dates for the name in column E (years listed separately, not as ranges)
    COLUMN G = Floor (values = 0-5)
    COLUMN H = Section (building number)
    COLUMN I = Section name
    COLUMN J = Hall number
    COLUMN K = Source (mostly abbreviated publications cited with year and page number: GG = General Guide, AR = Annual Report, OG = Official Guide)
    COLUMN L = Notes

---

### Data Fields mapped to EAC-CPF

    COLUMN A = control > recordId
    COLUMN B = cpfDescription > description > biogHist > p
    COLUMN C = cpfDescription > identity > nameEntry > part (with authorizedForm="amnhopac")
    COLUMN D = no map
    COLUMN E = cpfDescription > identity > nameEntry > part [if COLUMN L includes "amnhopac", then @authorizedForm="amnhopac"]
    COLUMN F = cpfDescription > identity > nameEntry > [part from COLUMN E] > useDates (multiple values separated by comma)
    COLUMN G = locally defined field or ["Floor "] cpfDescription > description > biogHist > p
    COLUMN H = locally defined field or ["Section "] cpfDescription > description > biogHist > p
    COLUMN I = locally defined field or ["Section name "] cpfDescription > description > biogHist > p
    COLUMN J = locally defined field or ["Hall number "] cpfDescription > description > biogHist > p
    COLUMN K = control > source > sourceEntry (multiple values separated by semicolon)
    COLUMN L = cpfDescription > description > bioghist > p"

---

