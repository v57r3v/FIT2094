java c
FIT2094 Databases 
Assignment 1    - Database Design 
Caring Hands Hospital (CHH) 

Purpose Given the provided case study, students will be asked to transform. the information provided into a sound database design and implement it in Oracle. This task covers learning outcomes: 
1.       Apply the theories of the relational database model. 
2. Develop a sound relational database design. 
3. Implement a relational database based on a sound database design. 
Your task 
This is an open-book, individual task.       The output for this task will be an initial 
conceptual model as a PDF document and    a logical model implemented in the Oracle RDBMS 
Value 
40 % of your total marks for the unit 
Due Date 
Wed, 5th Feb 2025 at 4:30 pm 
Submission 
● Via Moodle Assignment Submission. 
●          FIT GitLab check-ins will be used to assess the history of development 
Assessment Criteria 
●          Using the supplied case study description, prepare a conceptual model identifying the required entities, attributes and relationships. 
●          Normalise the supplied case study forms/s and integrate the resultant relations into a logical model derived from the identified conceptual model. 
●          Depict the data requirements expressed in the case study via a relational database logical model. 
●          Generate a schema that meets the case study data requirements from the logical model produced 
●          Consistent use of industry-standard notation and convention 
Late Penalties 
●          5% of the marks available for the task (-5 marks) deduction per calendar day or part thereof for up to one week 
●          Submissions over 7 calendar days after the due date will receive a mark of zero (0), and no assessment feedback will be provided. 
Support Resources 
See Moodle Assessment page 
Feedback 
Feedback will be provided on student work via: 
● general cohort performance


●          specific student feedback ten working days post-submission 
● a sample solution 
Case Scenario 
Caring   Hands   Hospital treats   patients who are   identified   by a unique   patient   id. When a patient   is admitted to the   hospital, the   hospital   records the   patient's first and last   name, address, date of birth and emergency contact   number   (if they are   not   already   on   the system). They also record the date and time   of admission.   The   system   needs   to   maintain   a   record of all admissions for a particular patient. When   a   patient   is   discharged,   the   date   and   time of their discharge for this admission is   recorded. 
While   in the   hospital   patients are   located   in a   bed within a ward.   Each ward   is   identified   by a   ward code.   Beds located   in a ward are assigned   a   bed   number within that ward   -   thus,   for   example, each ward   has a   bed   number   1. The   bedside   telephone   number and bed type   are      also   recorded.   During a stay   in the   hospital   patients   may   be   moved from one   bed to another   (this might involve   a   change   of   wards).
On admission each   patient   is assigned one doctor (identified   by   a   doctor   id)   as   their supervising doctor.   If a   patient   has   multiple admissions they   may   be assigned a different   supervising doctor with a different admission. A patient's supervising   doctor   may   be   in charge of many admissions. The hospital   records each   doctor's first   and   last   names   and   phone   number.
During their admission,   patients are   prescribed   procedures as   part of their care by   doctors   (a   procedure can only be   prescribed by a   doctor).   Procedures   consist   of tests   such   as "X-Rays", "Blood Tests" etc, they also   include   medical   procedures which   might   be required   such as "Shoulder Replacement". A patient   may   have   procedures   prescribed   by their supervising doctor or any other doctor working in the   hospital.
A   procedure   is   identified   by a   procedure code.   Each   procedure   has a   name (such as   "Wrist   X-Ray") and includes a description of what the   procedure   involves, the time   required for   the   procedure and the current standard patient cost for this   procedure.   When   a   particular procedure   is   prescribed during a   patient’s admission, the date and time when the   procedure   is carried out   is also   recorded.   For a given   patient, a   particular   procedure   is   completed before any further procedures are run   (two   procedures cannot   occur   simultaneously for   the same   patient). A doctor may require procedures   on   different   patients which   are   carried   out   at   the same time. Some   procedures, such as blood   tests   are   carried   out   by   technicians,   more complex   procedures   may require a doctor to perform. the   procedure. 
If a   procedure   is carried out   by a technician the   hospital does   not   record the   details   of the   technician who completed the procedure.
If a doctor carries out the procedure, the doctor who   completes   the   procedure   is   recorded (the doctor who completes the   procedure   may be different from the   doctor who   prescribes   it).   If a team of doctors   is   involved   in the   procedure, only one doctor (the   doctor   in   charge)   is recorded as completing the   procedure.
Caring   Hands   Hospital only   records the details of a   procedure carried out on   an   admission after the   procedure   has   been completed. The   patient cost for the   procedure   is recorded, this   may be different to the   standard   procedure   cost.
Not all admissions   require a   procedure to   be carried   out.
Procedures   may   require "extra"   items such as syringes or swabs.   Each   item   held   in stock   is   assigned an   item code. The   item description, current stock and   price   are   recorded.
REMEMBER to   keep up to date with the   Moodle   Ed Assignment   1 forum, where further   clarifications   may   be   posted (this forum is to be treated   as   your   client).
To view Assignment   1 only   posts, select the Assignment and then the Assignment   1 forum   from the Categories   list   in the   left   panel.
Once selected, you can   Filter the   posts via the   Filter option at the top   of the   list   of   posts:

Please be careful to ensure you do not publicly post anything that includes your reasoning, logic, or any part of your work to this forum. Doing so violates Monash plagiarism/ collusion rules and carries significant academic penalties. Use private posts to raise questions that may reveal part of your reasoning or solution. 
You are free to   make assumptions   if needed   however they   must align with the details   here and   in the assignment forums and   must be clearly documented   (see   the   required   submission   files). Normally such assumptions would only relate to minimum cardinality where not expressed in the case study. 
GIT STORAGE 
Your work for these tasks MUST be saved   in your Assignment   1 folder of your local repository and regularly pushed to the FIT GitLab server to build a   clear   history   of the   development of your model. 
TASKS to be Completed 
TASK 1 Caring Hands Hospital Conceptual Model [15 Marks] 
Based on the case scenario on pages   2   and   3   of this document   prepare   a CONCEPTUAL model for Caring   Hands   Hospital.   In   preparing this   model you must only use the description provided on pages 2 and 3.   Your model   must   be saved   in   a file   named chh_conceptual.pdf 
Your development   history as   pushed to Git   Lab   must clearly show the   steps   you   have   been   taught:
●          Step 1: entities and   keys
●         Step 2:   relationships, and
● Step 3:   non-key attributes
The PDF file of your model must have at least three pushes (remember all pushes must be of a file with the same name - chh_conceptual.pdf).   Please   note that   three pushes are a   minimum; you are free to   make   more (and we would   expect   more,   in which case you will   have   more than one commit/push for each step). You   must   regularly check   that   your pushes   have   been successful   by   logging   in to the   FIT Git   Lab server's web   interface; you   must   not simply assume they are working.   Do   not forget to check that   your   Git   Lab author details are correct for every   push.   Before submission via   Moodle, you   must   log   in to   the Git   Lab server's web   interface and ensure your final   submission   files   are   present. GIT automatically   maintains a   history of all files   pushed to the server. You   do   not   need to,   and   MUST   not, add a version   name to your various versions.   Please ensure you   use the      same name (chh_conceptual.pdf) for all versions of your solution.
The steps to complete this task: 
Using   LucidChart,   prepare a FULL conceptual model (Entity   Relationship   Diagram)   using   crow’s foot   notation for Caring   Hands   Hospital (CHH)    as described above.
●          For this FULL conceptual   model (ERD),   include:
○          identifiers (keys) for each   entity
○         all   required attributes, and
○         all   relationships. Cardinality (min and max)   and   connectivity for   all   relationships   must   be shown on the diagram.
● Surrogate keys must not be added to this model.
Your model must conform. to the unit ERD standards listed in the Applied 3: Conceptual Modelling (A3-2) lesson on ed. Your name must be shown on your diagram and it must be created as an A4 page. 
TASK 2 Caring Hands Hospital Normalisation [15 marks] 
The document shown on the   next   page   is   printed when a   patient   is about to   be   discharged   from the   hospital and contains all the procedures that   have   been   carried   out   during   their admission.

Perform. normalisation to 3NF for the data depicted in the   supplied   sample   document.   This   normalisation   must   be   based only on the depicted forms content - you   must   not   introduce attributes not shown on   the   document.
The approach you must use代 写FIT2094 Databases Assignment 1 - Database DesignSQL
代做程序编程语言 is shown   in the   normalisation applied class   solutions.   you   must   begin   by   representing the document you are working on as a   single   UNF   relation   and   then   move through   1NF, 2NF, and 3NF. No marks will be awarded if you use a different approach.
During normalisation, you   must:
○ Not add surrogate keys.
○ Include all attributes shown on the from (you   must not remove any   attribute   as   derivable)
○                            Clearly show UNF, 1NF, 2NF and 3NF.
○                            Clearly show all candidate keys for each   relation   in   1NF.
○ Identify the Primary Key in all relations by underlining the PK attribute/s.
○ Identify all dependencies at the various   normalisation stages   (Partial at   1NF,
Transitive at 2NF and   Full at 3NF). You should   use   the   same   notation   as   depicted   in   the normalisation sample solutions, for   example:
attr1 ->   attr2,   attr3
If none exist, you   must   note this   by   stating:
No partial dependencies present and/or No transitive dependencies present 
○ Carry out attribute synthesis if required.
The relation and attribute names used throughout your normalisation and those on your subsequent logical model must be the same.
Your normalisation   must   be carried out   in either an   MS Word or Apple   Pages   or   Google document with a filename of chh_normalisation.   If you are using   MS Word or   Pages (preferred)   place the source document   inside your local assignment   1   Git   Lab   repo. As you   develop your normalisation the source document   must be   regularly   saved   and   pushed to Git   Lab.   If you are using a Google document, you   must   regularly   download   the   normalisation   as a file called chh_normalisation.pdf and push   it   to   Git   Lab. 
Your normalisation must have at least three pushes (remember all pushes must be of a file with the same name - chh_normalisation ) to GitLab. The file extension for chh_normalisation will depend on which software you choose to use. Ensure that your name is shown on every page of the normalisation.
TASK 3 Caring Hands Hospital Logical Model [55 marks] 
Caring   Hands   Hospital   have supplied some further information to guide your modelling:
● For accounting   purposes, each   item   is assigned to a unique   cost   centre,   such   as
Pharmacy,    Radiography or Patient Aids. A cost   centre   is   identified   by   a   cost   centre code, your design   must also record the cost centre's   title   (such   as   Pharmacy)   and   the   manager's   name. CHH wishes to be able to add   new   cost   centres   as   needed.   They            wish the   manager's   name to   be treated as as simple attribute   ie.   not   be decomposed.
●          Beds at CHH are classified   (their bed   type)   as   either fixed   or   adjustable.   Not   all   beds   are supplied with a bedside telephone. CHH wish to   be   able   to   identify   the   date   and      time a   patient   is assigned to a   particular   bed.
●          Doctors titles   must   be one of:   Mr,   Mrs,   Ms,   Dr, AProf, or   Prof - this   range of titles will   not   be extended and will be stored as   listed   (not   abbreviated further).
1.          Prepare a   logical   level design for the Caring   Hands   Hospital database   based   on   your
Task   1   Conceptual   model, the   normalisations you carried out   in Task 2   above   and further   details supplied   here   in Task   3.
●                   The logical   model   must   be drawn   using the Oracle   Data   Modeler.   Information
engineering or Crow’s foot   notation   must   be   used to draw the   model. Your logical   model   must not show data types. You must create a new empty folder, in your local repo, in the Ass1 folder, called chh_model, and then place your model inside this folder naming the saved model as chh_logical. 
●                   All   relations depicted   must   be   in 3NF. Candidate   keys   are   possible   natural   keys; you must ensure your model protects all candidate keys to   maintain   the business   rules.
●                   You   must add at least one surrogate key to your design (you   are   free   to
select the   most appropriate   relation to   make this change   in). You must explain why you added the surrogate key to your chosen relation as part of your assumptions. We   have a unit   rule about   requiring a surrogate   key   if the   relation has a composite   key with   more than two attributes,   but this   is   not the   only   reason   you   might add a surrogate. You   may add surrogate   keys to   multiple   relations   if you wish.
●                   All attributes must be commented in the database (i.e., the   comments   must   be   part of the table structure, not simply comments   in the   schema file).
●                   Check clauses/look-up tables must   be   applied   to   attributes where   appropriate.
●                   You MUST include the   legend   in your model.   Please edit   the   legend   panel   to show   your   name   and   ID   number.
● Please carefully check the slide "Overall Design Process - checklist" from the Topic 5 Workshop and ensure you follow the steps listed. 
●                   Your GIT repository   must   indicate your development   history with   multiple
commits/pushes as you work on your model. A minimum of six pushes is 
required for your logical model, as it is developed, so as to show this 
history. You are free to make more pushes/commits and are encouraged to do so. 
2. Generate the database schema in Oracle Data Modeler and use the schema to create the database in your Oracle account.
The only edit you are permitted to carry   out to   the   generated   schema file   is   to   add header comment/s containing your details and   the commands to spool/echo   your   run   of   the script. (as   illustrated   in Applied 6   Logical   Modelling).   In generating your schema file,      ensure you:
●                   Capture the output of the   run of your schema   statements   using the   spool   command.
●                   Ensure your script. includes   drop   table   statements   at   the   start   of the   script.
●                   Name the schema file   as chh_schema.sql. 
Please note when working with your model, ensure that you NEVER select any export options from the Data Modeler menu:

such actions can fill your Oracle account space and   render   it   unusable.
Tasks 1, 2 and 3 - Use of Modeling Standards/Meeting Submission Requirements and Git usage [15 marks] 
See the   Marking Guide section of this document for further details.
Use of Generative AI tools In this assessment, you can use generative artificial   intelligence   (AI)   in   order   to   assist   with   design decisions only. Any use of generative AI must be appropriately acknowledged (seeLearn   HQ)
Submission Requirements 
The following seven files are to be submitted and must also exist in   your   FITGit   Lab   server   repo:
● A single-page pdf file containing your full final conceptual model.      Name the file
chh_conceptual.pdf. This file   must   be created via   File -   Export (or   Download As) -            PDF from   LucidChart (do not use screen capture) and   must   be able to   be   accessed   with a development   history via GIT. You can create   this   development   history   by downloading your PDFs (don't forget to use the same name chh_conceptual.pdf 
- DO NOT use version 1 etc) and committing/pushing to GIT as   you work   on   your   model.   In exporting from   LucidChart, please select a page size of A4.
● A PDF document showing your full normalisation of the sample "Admission
Procedure Charge Sheet" document showing all   normal forms   (UNF,   1NF,   2NF   and   3NF).   Name the file chh_normalisation.pdf 
●      A single-page PDF file containing the final logical   Model you   created   in   Oracle   Data   Modeler.   Name the file chh_logical.pdf. This   pdf must   be created via   File -   Data
Modeler -   Print   Diagram - To   PDF   File from within   Data   Modeler, do   not   use screen   capture.
●      A zip file containing your Oracle   Data   Modeler project (when   zipping   these   files,   be   sure to   include the   .dmd file and the folder of the same name).   Name   the   zip file
chh_model.zip. 
Part of the assessment of your submission will involve your marker extracting   your            model from this zip, opening   it   in   Data   Modeller, and engineering to a   new   Relational   model.   From this, your marker will generate a schema, which will then   be compared      with your submitted schema (they must be the same for your schema to be 
accepted).   For this   reason, your model must be able to be opened by your 
marker and contain your complete model (i.e. both your logical and relational models) otherwise, your submission will not be able to be fully marked, 
resulting in significant loss of marks.   You MUST carefully check that your   model         is complete - ensure you take your submission archive, copy it to a new temporary folder, extract your submission parts, extract your model   and   ensure   it   opens
correctly before submission.   Please view the video on   Ed under the   lesson   "A6   Oracle   Data   Modeler Support Videos", which demonstrates this process.
●         A schema file (CREATE TABLE statements) generated   by   Oracle   Data   Modeler.   Name the file chh_schema.sql 
●         The output from the Oracle spool command showing the   tables   have   been   created.   Name the file chh_schema_output.txt 
● A   PDF document containing any assumptions you wish to   make your   marker aware   of.   Name the file chh_assumptions.pdf.   If you   have   made   no assumptions, submit   the document with a single statement saying, "No assumptions   made".
Your assignment MUST show a status of "Submitted for grading"   before   it will   be   marked.

If your submission shows a status of "Draft (not   submitted)",   it will   not   be   assessed   and will incur late penalties after the due date/time.


         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
