# CBT015
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. GitHub repos will be deleted and created during this period...

```
//***FILE 015 IS FROM WARNER BROTHERS INC OF BURBANK, CA AND        *   FILE 015
//*           CONTAINS SEVERAL OF THEIR UTILTIES.  THIS FILE IS     *   FILE 015
//*           IN IEBUPDTE SYSIN FORMAT.                             *   FILE 015
//*                                                                 *   FILE 015
//*           TABLES AND JOBS NECESSARY TO GET SMF TYPE 32 TSO      *   FILE 015
//*           COMMAND ACCOUNTING RECORDS RUNNING.  USEFUL TO SEE    *   FILE 015
//*           WHAT RESOURCES OEM TSO PRODUCTS USE.                  *   FILE 015
//*                                                                 *   FILE 015
//*           A FEW PDF EDIT MACROS AND HELP MEMBERS.  A PDF        *   FILE 015
//*           FRONT END FOR DYNASOFT'S TSO WORD PROCESSOR AND       *   FILE 015
//*           SPREADSHEET.  A PRIMARY PDF PANEL THAT CAN SCROLL     *   FILE 015
//*           IN ALL FOUR DIRECTIONS TO ALLOW DISPLAY OF LOTS OF    *   FILE 015
//*           PDF OPTIONS.                                          *   FILE 015
//*                                                                 *   FILE 015
//*           A COUPLE OF ACF2 ASM ROUTINES TO DO RESOURCE          *   FILE 015
//*           VALIDATION AND INQUIRY FUNCTIONS.                     *   FILE 015
//*                                                                 *   FILE 015
//*           VERSION OF CLIP THAT WORKS WITH DSF REL9 AND XA OR    *   FILE 015
//*           370.                                                  *   FILE 015
//*                                                                 *   FILE 015
//*           TWO JES EXITS.  ONE PROVIDES A MASKABLE VERSION OF    *   FILE 015
//*           $D'NAME***.  WAS A SOURCE MOD TO HASPCOMM             *   FILE 015
//*           RE-WRIITEN AS AN EXIT.  EXIT FOUR ALLOWS FOR CODING   *   FILE 015
//*           DSN= ON SETUP CARDS.  EXIT CONVERTS DSN NAMES TO      *   FILE 015
//*           VOLSER'S SO USER DOES NOT HAVE TO LOOK THEM UP.       *   FILE 015
//*           SOME LOCAL CODE IN THIS BUT WOULD BE EASY TO DROP     *   FILE 015
//*           OR CHANGE.                                            *   FILE 015
//*                                                                 *   FILE 015
//*           MVS/XA MOD TO INSTALL CUSTOM CONSOLE PFK DEFINITIONS. *   FILE 015
//*           ONE SAMPLE DEFINITION INCLUDED.  THIS ALLOWS FOR      *   FILE 015
//*           SIMPLE RE-DEFINES AFTER GENS OR MAINTENANCE.  WE      *   FILE 015
//*           HAVE TEN CONSOLES SO THIS HELPS.                      *   FILE 015
//*                                                                 *   FILE 015
//*           MVS/XA MOD TO ALLOW RESTART OF JOBS THAT USE GDG'S    *   FILE 015
//*           AND REFER TO THEM AS +1 IN LATER STEPS.  WITHOUT      *   FILE 015
//*           THIS MOD JOBS RESTARTED WOULD HAVE TO HAVE ALL        *   FILE 015
//*           REFERENCES TO +1 CHANGED TO 0.  THIS IS AN ERROR      *   FILE 015
//*           PRONE AND TIME CONSUMING TASK.  TESTED AND RUNNING    *   FILE 015
//*           UNDER XA 2.1.7 DFP 2.2.3.  THIS IS A VERY STABLE      *   FILE 015
//*           MOD.  HAS NOT CHANGE SIZE OR LOCATION IN YEARS.       *   FILE 015
//*           LAST CHANGE WAS A "DISPLACEMEMNT" CHANGE WHEN SIZE    *   FILE 015
//*           OF MODULE WAS CHANGED.                                *   FILE 015
//*                                                                 *   FILE 015
//*           MEMBER                     DESCRIPTION                *   FILE 015
//*           $JCL           JCL USED TO CREATE THIS FILE.          *   FILE 015
//*           $DSCLAIM       STANDARD CYA DISCLAIMER                *   FILE 015
//*           $README        THIS STUFF                             *   FILE 015
//*           #RESTORE       HELP FOR RESTORE EDIT MACRO.           *   FILE 015
//*           #TRAP          HELP FOR TRAP EDIT MACRO.              *   FILE 015
//*           #VPS           HELP FOR VPS  EDIT MACRO.              *   FILE 015
//*           ACF2INQ        ASM SUBROUTINE TO RETURN ACF2 UID      *   FILE 015
//*                          STRING TO A REQUESTING CICS            *   FILE 015
//*                          TRANSACTION.                           *   FILE 015
//*           ACF2VALD       ASM PGM THAT DOES A RESOURCE           *   FILE 015
//*                          VALIDATION FROM BATCH OR TSO.  CAN     *   FILE 015
//*                          BE USED TO CONTROL POWERFUL TSO CP'S   *   FILE 015
//*                          LIKE SPY, QUEUE, ETC. OR TO CONTROL    *   FILE 015
//*                          BATCH ACCESS TO CRITICAL RESOURCES.    *   FILE 015
//*           ASKUID         ASM SUBROUTINE TO RETURN ACF2 UID      *   FILE 015
//*                          STRING TO AS A PDF DIALOG VARIABLE.    *   FILE 015
//*           CLIP           ASM PGM RUNS AS A STARTED TASK.        *   FILE 015
//*                          USED TO RELABEL OR INSPECT DASD FROM   *   FILE 015
//*                          A CONSOLE. RUNS OK WITH DSF REL9.      *   FILE 015
//*           DYN#C1         PDF CLIST TO INVOKE DYNASOFT PRODUCT   *   FILE 015
//*           DYN#P1         PRIMARY DYNAPLAN PANEL                 *   FILE 015
//*           DYN#T1         FIRST PANEL OF PROPOSED TUTORIAL       *   FILE 015
//*                          SERIES, WOULD ALSO BE A SELECTABLE     *   FILE 015
//*                          OPTION OF DYN#P1.                      *   FILE 015
//*           DYNASEND       JCL USED TO CREATE THIS FILE           *   FILE 015
//*           DYNM00         PDF MESSAGE MEMBER                     *   FILE 015
//*           GDGMOD         VERY USEFUL MOD TO SIMPLIFY            *   FILE 015
//*                          RESTARTING JOBS THAT USE GDG'S.        *   FILE 015
//*           IEEMB846       SOURCE FOR TSO ACCOUNTING TABLE.       *   FILE 015
//*           IEEPK860       SAMPLE INPUT TO CONSOLE PFK MOD.       *   FILE 015
//*           ISPTCM         SOURCE FOR ISPF ACCOUNTING TABLE       *   FILE 015
//*           ISR*PRIM       SAMPLE PRIMARY PANEL USED TO INVOKE    *   FILE 015
//*                          OPTION "DYNA".  KIND OF NEAT AS IT'S   *   FILE 015
//*                          SCROLLABLE IN FOUR DIRECTIONS.         *   FILE 015
//*           JCLJES4        JCL TO ASM + LINK JES EXIT 4           *   FILE 015
//*           JCLJES5        JCL TO ASM + LINK JES EXIT 5           *   FILE 015
//*           JESXIT5D       ADD $D'JOB**** COMMAND TO JES2.        *   FILE 015
//*           JES2XIT4       MOD TO ALL DSN= ON SETUP CARDS IN JES  *   FILE 015
//*                          MAKES IT MUCH EASIER TO PULL TAPES     *   FILE 015
//*                          FOR PRODUCTION JOBS. HAS SOME SITE     *   FILE 015
//*                          DEPENDENT CODE IN IT.                  *   FILE 015
//*           PRIMDOWN       SAMPLE PRIM DOWN PANEL                 *   FILE 015
//*           PRIMLEFT       SAMPLE PRIM LEFT PANEL                 *   FILE 015
//*           PRIMRGHT       SAMPLE PRIM RGHT PANEL                 *   FILE 015
//*           PRIMUP         SAMPLE PRIM UP PANEL                   *   FILE 015
//*           RESTORE        EDIT MACRO.  RELOADS LAST SAVED COPY   *   FILE 015
//*                          OF CURRENT MEMBER.  FASTER THAN DOING  *   FILE 015
//*                          A CANCEL AND SELECTING MEMBER OVER     *   FILE 015
//*                          AGAIN.                                 *   FILE 015
//*           SMFPRM00       SAMPLE SMF PARMS.  NOTE ATE DETAIL     *   FILE 015
//*                          MUST BE CODED FOR TCB, IO, ECT. TO     *   FILE 015
//*                          BE RECORDED IN SMF32.                  *   FILE 015
//*           SMF32SAS       SAS PGM TO ANALYSIS SMF32 RECORDS.     *   FILE 015
//*           SMPEIEE        SAMPLE SMPEJCL TO INSTALL IEEMB846     *   FILE 015
//*           SMPEPFK        SAMPLE SMPEJCL TO INSTALL CONSOLE      *   FILE 015
//*                          PFK MOD.                               *   FILE 015
//*           SMPETCM        SAMPLE SMPEJCL TO INSTALL ISPTCM       *   FILE 015
//*           SWTSO          SOURCE CODE TO SMF FRONT END PGM.      *   FILE 015
//*                          THIS IS A GENERAL PURPOSE PGM WHICH    *   FILE 015
//*                          SETS UP THE SMF32 ENVIRONMENT.         *   FILE 015
//*                          BECAUSE OF INTERNAL WB STANDARDS A     *   FILE 015
//*                          LMODLIB DD STATEMENT IS REQUIRED.      *   FILE 015
//*                          THE CODE COULD VERY EASILY BE ADDED    *   FILE 015
//*                          TO DYNAPLAN OR THE FRONTEND PGM        *   FILE 015
//*                          SUPPLIED AS A USER OPTION.  THE SVC    *   FILE 015
//*                          STARTS AND STOPS SMF32 ACCOUNTING.     *   FILE 015
//*           TRAP           EDIT MACRO.  WILL TRAP THE OUTPUT OF   *   FILE 015
//*                          A TSO CP AND PLACE IT AT THE BOTTOM    *   FILE 015
//*                          OF THE CURRENT EDIT DATASET.  GOOD     *   FILE 015
//*                          EXAMPLE OF SOME OF THE NEAT THINGS     *   FILE 015
//*                          YOU CAN DO UNDER TSO/E.  WILL ONLY     *   FILE 015
//*                          WORK WITH TSO CP'S THAT USE PUTLINE.   *   FILE 015
//*                          WILL NOT WORK WITH FULLSCREEN          *   FILE 015
//*                          TPUT'S.                                *   FILE 015
//*           VPS            EDIT MACRO.  QUICK WAY TO GET A        *   FILE 015
//*                          VPSPRINT OF CURRENT EDIT DATA.  NOTE:  *   FILE 015
//*                          DOES A SAVE FIRST.  THIS TECHNIQUE     *   FILE 015
//*                          COULD BE USED FOR ANY TSOCP OR         *   FILE 015
//*                          UTILITY.                               *   FILE 015
//*                                                                 *   FILE 015
```
