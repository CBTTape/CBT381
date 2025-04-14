# CBT381
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 381 IS FROM FIRST COMPUTER SERVICES AND CONTAINS A COPY   *   FILE 381
//*           OF SOME OF THEIR PROGRAMS, UTILITIES AND JES2 EXITS.  *   FILE 381
//*           THIS FILE IS IN IEBUPDTE SYSIN FORMAT AND HAS BEEN    *   FILE 381
//*           PROCESSED BY OFFLOAD.  IT CONTAINS THE FOLLOWING:     *   FILE 381
//*                                                                 *   FILE 381
//*     THE JES2 EXITS PREFIXED WITH 'JES' ARE FOR MVS SP 1.3.4     *   FILE 381
//*     (HJE2330), SP 1.3.6 (HJE1367) OR SP 2.1.5 (HJE2157).        *   FILE 381
//*     THESE EXITS ARE ALMOST IDENTICAL IN FUNCTION TO THE         *   FILE 381
//*     ORIGINAL EXITS WHICH HAVE BEEN AVAILABLE FOR SEVERAL        *   FILE 381
//*     YEARS.  BECAUSE OF CHANGING REQUIREMENTS, THESE EXITS HAVE  *   FILE 381
//*     CHANGED IN OUR CURRENT ENVIRONMENT AND THERE IS NO WAY TO   *   FILE 381
//*     INCORPORATE CHANGES OR ENHANCEMENTS INTO THE OLD EXITS.     *   FILE 381
//*     THEY WILL BE INCLUDED ONLY FOR THOSE WHO MAY WANT TO        *   FILE 381
//*     COMPARE THE NEW VERSION OF THE EXITS TO THE OLD ONES.       *   FILE 381
//*                                                                 *   FILE 381
//*     THE NEW EXITS ARE SET FOR SP 2.2.0 (HJE2221) ALTHOUGH THE   *   FILE 381
//*     CHANGES FROM SP 2.1.5 WERE MINOR.                           *   FILE 381
//*                                                                 *   FILE 381
//*     A NUMBER OF JES2 COMMANDS WERE ADDED TO PROVIDE MORE        *   FILE 381
//*     DETAILED INFORMATION OR SUPPORT FOR ADDITIONAL FACILITIES.  *   FILE 381
//*     A BRIEF LIST FOLLOWS:                                       *   FILE 381
//*                                                                 *   FILE 381
//*     $LF    - A DETAILED VERSION OF THE IBM $DF COMMAND GIVING   *   FILE 381
//*              JOBNAME, LINE OR PAGE COUNT AS WELL AS OTHER       *   FILE 381
//*              INFORMATION.                                       *   FILE 381
//*                                                                 *   FILE 381
//*     $DV    - A COMMAND THAT CAN LIST DASD VOLUMES BY DEVICE     *   FILE 381
//*              ADDRESS OR BY VOLSER OR PREFIX.  IT IS HARD TO     *   FILE 381
//*              FIND A SPECIFIC DASD VOLSER WHEN USING THE MVS     *   FILE 381
//*              'D U' COMMAND.                                     *   FILE 381
//*                                                                 *   FILE 381
//*     $QJ    - A FUNCTIONAL REPLACEMENT FOR THE IBM $DJ COMMAND.  *   FILE 381
//*              THIS VERSION LISTS ADDITIONAL INFORMATION TO       *   FILE 381
//*              SUPPORT THE MULTIPLE CATAGORIES OF HOLD, FAILURE   *   FILE 381
//*              FLAGS, TEST OR PRODUCTION INDICATORS AND OWNER     *   FILE 381
//*              ID.                                                *   FILE 381
//*                                                                 *   FILE 381
//*     $QN    - A FUNCTIONAL REPLACEMENT FOR THE IBM $DN COMMAND.  *   FILE 381
//*              THIS VERSION LISTS ADDITIONAL INFORMATION TO       *   FILE 381
//*              SUPPORT THE MULTIPLE CATAGORIES OF HOLD, FAILURE   *   FILE 381
//*              FLAGS, TEST OR PRODUCTION INDICATORS AND OWNER     *   FILE 381
//*              ID.                                                *   FILE 381
//*                                                                 *   FILE 381
//*     $SL    - SUPPORT FOR THE SETUP HOLD FACILITY.  THIS         *   FILE 381
//*              COMMAND WILL EITHER LIST ALL JOBS ON THE SETUP     *   FILE 381
//*              HOLD QUEUE OR LIST THE ACTUAL /*SETUP CONTROL      *   FILE 381
//*              CARDS FOR AN INDIVIDUAL JOB.                       *   FILE 381
//*                                                                 *   FILE 381
//*     $SR    - SUPPORT FOR THE SETUP HOLD FACILITY.  THIS         *   FILE 381
//*              COMMAND WILL RELEASE JOBS FROM THE SETUP HOLD      *   FILE 381
//*              QUEUE.                                             *   FILE 381
//*                                                                 *   FILE 381
//*     $UL    - SUPPORT FOR THE USER HOLD FACILITY.  THIS COMMAND  *   FILE 381
//*              WILL LIST JOBS IN THE USER HOLD QUEUE.             *   FILE 381
//*                                                                 *   FILE 381
//*     $UA    - SUPPORT FOR THE USER HOLD FACILITY.  THIS COMMAND  *   FILE 381
//*              WILL PLACE JOBS IN THE USER HOLD QUEUE.            *   FILE 381
//*                                                                 *   FILE 381
//*     $UR    - SUPPORT FOR THE USER HOLD FACILITY.  THIS COMMAND  *   FILE 381
//*              WILL RELEASE JOBS FROM THE USER HOLD QUEUE.        *   FILE 381
//*                                                                 *   FILE 381
//*     $TJIT  - SUPPORT FOR THE JOB INFORMATION TASK OR VSAM       *   FILE 381
//*              DISTRIBUTION FILE FACILITY.  THIS COMMAND CAN      *   FILE 381
//*              START, STOP, RESTART, LIST STATUS, OR LIST THE     *   FILE 381
//*              DETAIL RECORD FROM THE VSAM FILE.                  *   FILE 381
//*                                                                 *   FILE 381
//*     $LOAD  - ALLOW JES2 EXITS TO BE RELOADED WITHOUT            *   FILE 381
//*              PERFORMING A JES2 HOT START.                       *   FILE 381
//*                                                                 *   FILE 381
//*     $TUCC7 - SUPPORT FOR THE UCC-7 (CA-7) INTERFACE.  THIS      *   FILE 381
//*              COMMAND CAN START, STOP, RESTART, OR LIST THE      *   FILE 381
//*              STATUS OF THE INTERFACE.                           *   FILE 381
//*                                                                 *   FILE 381
//*     JES$LF   - (OLD) A JES2 EXIT (5) TO PROVIDE OPERATOR        *   FILE 381
//*                CAPABILITY TO DISPLAY DETAILED INFORMATION       *   FILE 381
//*                ABOUT JOBS IN THE PRINT QUEUE.  IT IS DESIGNED   *   FILE 381
//*                TO ENHANCE THE DISPLAY NORMALLY PROVIDED BY THE  *   FILE 381
//*                $DF COMMAND.                                     *   FILE 381
//*                                                                 *   FILE 381
//*     JESEXIT1 - (OLD) A JES2 EXIT (1) TO PROVIDE ENHANCEMENTS    *   FILE 381
//*                TO THE IBM SUPPLIED SEPARATOR PAGE.  SUPPORT IS  *   FILE 381
//*                ALSO PROVIDED FOR THE KODAK KOMSTAR MICROFICHE   *   FILE 381
//*                PROCESSOR, THE DATAGRAPHIX ARIS II MICROFICHE    *   FILE 381
//*                PROCESSOR, THE IBM 6670 DOCUMENTATION PROCESSOR  *   FILE 381
//*                AND THE XEROX 9700 PRINTER.                      *   FILE 381
//*                                                                 *   FILE 381
//*     JESEXIT3 - (OLD) A JES2 EXIT (3) TO CREATE AN NJE JOB       *   FILE 381
//*                HEADER TO SAVE JOB ACCOUNTING INFORMATION        *   FILE 381
//*                LONGER THAN 4 CHARACTERS.  NOTE THAT THIS EXIT   *   FILE 381
//*                IS USED IN CONJUNCTION WITH JESEXIT7 TO PRODUCE  *   FILE 381
//*                AN SMF TYPE 30 RECORD FOR NJE PRINT JOBS AT THE  *   FILE 381
//*                RECEIVING NODE TO ALLOW JOB ACCOUNTING FOR NJE   *   FILE 381
//*                PRINT.                                           *   FILE 381
//*                                                                 *   FILE 381
//*     JESEXIT5 - (OLD) A JES2 EXIT (5) TO FILTER JES2 COMMANDS    *   FILE 381
//*                TO DISALLOW CERTAIN COMMANDS OR OPERANDS ON THE  *   FILE 381
//*                COMMANDS.                                        *   FILE 381
//*                                                                 *   FILE 381
//*     JESEXIT6 - (OLD) A JES2 EXIT (6) TO PERFORM STANDARDS       *   FILE 381
//*                ENFORCEMENT FOR JCL AS WELL AS SET THE JOB       *   FILE 381
//*                CLASS BASED UPON THE RESOURCES SUCH AS TAPE      *   FILE 381
//*                UNITS, REGION SIZE, OR CPU TIME.  VIOLATIONS TO  *   FILE 381
//*                STANDARDS AND JOB CLASS REPORTING IS MADE TO     *   FILE 381
//*                THE JOB MESSAGE DATA SET FOR THE JOB AS IF THE   *   FILE 381
//*                CONVERTER WAS PRODUCING THE ERROR MESSAGES.      *   FILE 381
//*                                                                 *   FILE 381
//*     JESEXIT7 - (OLD) A JES2 EXIT (7) TO CREATE AN SMF TYPE 30   *   FILE 381
//*                RECORD FOR NJE PRINT JOBS AT THE RECEIVING NODE  *   FILE 381
//*                TO ALLOW JOB ACCOUNTING FOR NJE PRINT.  NOTE     *   FILE 381
//*                THAT THIS EXIT IS USED IN CONJUNCTION WITH       *   FILE 381
//*                JESEXIT3 TO PROVIDE JOB ACCOUNTING INFORMATION.  *   FILE 381
//*                                                                 *   FILE 381
//*     JESEXIT9 - (OLD) A JES2 EXIT (9) TO ABEND TEST JOBS WHICH   *   FILE 381
//*                EXCEED THE ESTIMATED LINE COUNT WHILE ALLOWING   *   FILE 381
//*                ALL OTHER JOBS TO CONTINUE.                      *   FILE 381
//*                                                                 *   FILE 381
//*     JESXIT17 - (OLD) A JES2 EXIT (17) TO VALIDATE THE SIGNON    *   FILE 381
//*                CARD FROM BSC RJE WORKSTATIONS.  THIS EXIT WILL  *   FILE 381
//*                ISSUE A CALL TO ACF2 TO VALIDATE THE PASSWORD    *   FILE 381
//*                FOR THE REMOTEID.  THE SIGNON ATTEMPT WILL BE    *   FILE 381
//*                REJECTED WITH APPROPRIATE MESSAGES IF THE        *   FILE 381
//*                PASSWORD IS INVALID.                             *   FILE 381
//*                                                                 *   FILE 381
//*     JESXIT21 - (OLD) A JES2 EXIT (21) TO EXAMINE JES2 SMF       *   FILE 381
//*                RECORDS TO INSERT JOBNAME IN THE SMF TYPE57      *   FILE 381
//*                RECORD.  THIS NJE SYSOUT TRANSMISSION RECORD     *   FILE 381
//*                CONTAINS JOB NUMBER BUT NO JOB NAME.  IT IS      *   FILE 381
//*                DIFFICULT TO PRODUCE NJE STATISTICS WITHOUT      *   FILE 381
//*                THE JOBNAME.                                     *   FILE 381
//*                                                                 *   FILE 381
//*     J001$SP  - A JES2 EXIT (1) TO PROVIDE ENHANCEMENTS TO THE   *   FILE 381
//*                IBM SUPPLIED SEPARATOR PAGE.  THIS EXIT WILL     *   FILE 381
//*                REQUEST DISTRIBUTION INFORMATION FROM A JES2     *   FILE 381
//*                TASK WHICH EXTRACTS THIS INFORMATION FROM A      *   FILE 381
//*                VSAM FILE.  SUPPORT IS ALSO PROVIDED FOR THE     *   FILE 381
//*                KODAK KOMSTAR MICROFICHE PROCESSOR, THE          *   FILE 381
//*                DATAGRAPHIX ARIS II MICROFICHE PROCESSOR, THE    *   FILE 381
//*                XEROX 3700 PRINTER AND THE XEROX 9700 PRINTER.   *   FILE 381
//*                ALSO REQUIRES EXITS HASPXIT0, J024JIT, J015$SP   *   FILE 381
//*                (FOR 3700 SUPPORT), J005JIT, AND J005UCC7 FOR    *   FILE 381
//*                FULL SUPPORT.  THERE ARE SEVERAL ASSEMBLY        *   FILE 381
//*                VARIABLES IN THE EXIT TO SET OPTIONS.  SEE       *   FILE 381
//*                THE COMMENTS IN THE PROGRAM.                     *   FILE 381
//*                                                                 *   FILE 381
//*     J003STCS - A JES2 EXIT (3) TO SET THE DEFAULT SYSOUT CLASS  *   FILE 381
//*                AND PROGRAMMER NAME FOR STARTED TASKS.  THIS     *   FILE 381
//*                INFORMATION IS PROVIDED BY A JES2 TASK WHICH     *   FILE 381
//*                EXTRACTS THIS INFORMATION FROM A VSAM FILE.      *   FILE 381
//*                THIS ALLOWS SOME STARTED TASKS TO DEFAULT TO A   *   FILE 381
//*                THROWAWAY SYSOUT CLASS AND OTHERS TO PRINT.      *   FILE 381
//*                THIS EXIT ALSO REQUIRES EXITS HASPXIT0 J024JIT,  *   FILE 381
//*                J005JIT, AND J005UCC7 FOR FULL SUPPORT.          *   FILE 381
//*                                                                 *   FILE 381
//*     J003UNJH - A JES2 EXIT (3) TO CREATE AN NJE JOB HEADER TO   *   FILE 381
//*                SAVE JOB RELATED INFORMATION ACCROSS AN NJE      *   FILE 381
//*                ENVIRONMENT AND SPOOL OFFLOAD/RELOAD             *   FILE 381
//*                OPERATIONS.  THIS INFORMATION JOB ACCOUNTING     *   FILE 381
//*                INFORMATION LONGER THAN 4 CHARACTERS, AND        *   FILE 381
//*                INSTALLATION FIELDS IN THE JQE.  THE ACCOUNTING  *   FILE 381
//*                INFORMATION IS USED BY EXIT J007JQEU TO PRODUCE  *   FILE 381
//*                AN SMF TYPE 30 RECORD FOR NJE PRINT JOBS AT THE  *   FILE 381
//*                RECEIVING NODE TO ALLOW JOB ACCOUNTING FOR NJE   *   FILE 381
//*                PRINT.                                           *   FILE 381
//*                                                                 *   FILE 381
//*     J004$JEC - A JES2 EXIT (4) TO PROCESS THE DEPENDENT JOB     *   FILE 381
//*                CONTROL JECL STATEMENTS.  THIS EXIT WILL         *   FILE 381
//*                PROCESS THE /*SETUP, /*THREAD, /*EXCLUDE, AND    *   FILE 381
//*                /*RELEASE JECL STATEMENTS.  THIS EXIT FILLS IN   *   FILE 381
//*                MANY OF THE USER FIELDS IN THE MODIFIED JQE.     *   FILE 381
//*                ALSO REQUIRES EXITS J005$SL, J005$SR, J007RLSE,  *   FILE 381
//*                J014$JCL, AND J020UHLD FOR FULL SUPPORT.         *   FILE 381
//*                                                                 *   FILE 381
//*     J004$OWN - A JES2 EXIT (4) TO LOCAL EXTENSIONS TO THE       *   FILE 381
//*                /*JOBPARM JECL STATEMENT.  THESE FIELDS ARE      *   FILE 381
//*                OWNERID, FCB, AND UCS.  THIS ALLOWS XBATCH JOBS  *   FILE 381
//*                TO SPECIFY EXTRA JOB ATTRIBUTES.                 *   FILE 381
//*                                                                 *   FILE 381
//*     J005$DV  - A JES2 EXIT (5) TO PROVIDE OPERATOR CAPABILITY   *   FILE 381
//*                TO DISPLAY DASD VOLUMES BY DEVICE ADDRESS,       *   FILE 381
//*                VOLSER, OR VOLSER PREFIX.  THE MVS 'D U'         *   FILE 381
//*                COMMAND IS CUMBERSOME WHEN LOOKING FOR           *   FILE 381
//*                SPECIFIC VOLUMES.                                *   FILE 381
//*                                                                 *   FILE 381
//*     J005$LF  - A JES2 EXIT (5) TO PROVIDE OPERATOR CAPABILITY   *   FILE 381
//*                TO DISPLAY DETAILED INFORMATION ABOUT JOBS IN    *   FILE 381
//*                THE PRINT QUEUE.  IT IS DESIGNED TO ENHANCE THE  *   FILE 381
//*                DISPLAY NORMALLY PROVIDED BY THE $DF COMMAND.    *   FILE 381
//*                                                                 *   FILE 381
//*     J005$QJ  - A JES2 EXIT (5) TO PROVIDE A FUNCTIONAL          *   FILE 381
//*                REPLACEMENT FOR THE IBM $DJ COMMAND.  IT WAS     *   FILE 381
//*                WRITTEN TO PROVIDE A MEANS TO DISPLAY THE JOB    *   FILE 381
//*                RELATED INFORMATION ADDED BY OUR INSTALLATION.   *   FILE 381
//*                                                                 *   FILE 381
//*     J005$QN  - A JES2 EXIT (5) TO PROVIDE A FUNCTIONAL          *   FILE 381
//*                REPLACEMENT FOR THE IBM $DN COMMAND.  IT WAS     *   FILE 381
//*                WRITTEN TO PROVIDE A MEANS TO DISPLAY THE JOB    *   FILE 381
//*                RELATED INFORMATION ADDED BY OUR INSTALLATION.   *   FILE 381
//*                                                                 *   FILE 381
//*     J005$SL  - A JES2 EXIT (5) TO PROVIDE A WAY TO LIST ALL     *   FILE 381
//*                JOBS IN A USER DEFINED QUEUE CALLED THE SETUP    *   FILE 381
//*                QUEUE.  THIS QUEUE PREVENTS JOBS FROM EXECUTING. *   FILE 381
//*                IT ALSO ALLOWS THE CONSOLE OPERATOR THE ABILITY  *   FILE 381
//*                TO RELIST THE /*SETUP CARDS FOR EACH JOB.        *   FILE 381
//*                                                                 *   FILE 381
//*     J005$SR  - A JES2 EXIT (5) TO PROVIDE A WAY TO RELEASE A    *   FILE 381
//*                JOB FROM A USER DEFINED QUEUE CALLED THE SETUP   *   FILE 381
//*                QUEUE.  THIS QUEUE PREVENTS JOBS FROM EXECUTING. *   FILE 381
//*                                                                 *   FILE 381
//*     J005$UA  - A JES2 EXIT (5) TO PROVIDE A WAY TO REMOVE A     *   FILE 381
//*                JOB FROM A USER DEFINED QUEUE CALLED THE USER    *   FILE 381
//*                HOLD QUEUE.  THIS QUEUE PREVENTS A JOB FROM      *   FILE 381
//*                EXECUTING (NOT FROM PRINTING).                   *   FILE 381
//*                                                                 *   FILE 381
//*     J005$UH  - A JES2 EXIT (5) TO PROVIDE A WAY TO PLACE A      *   FILE 381
//*                JOB IN A USER DEFINED QUEUE CALLED THE USER      *   FILE 381
//*                HOLD QUEUE.  THIS QUEUE PREVENTS A JOB FROM      *   FILE 381
//*                EXECUTING (NOT PRINTING).                        *   FILE 381
//*                                                                 *   FILE 381
//*     J005$UL  - A JES2 EXIT (5) TO PROVIDE A WAY TO LIST ALL     *   FILE 381
//*                JOBS IN A USER DEFINED QUEUE CALLED THE USER     *   FILE 381
//*                HOLD QUEUE.  THIS QUEUE PREVENTS A JOB FROM      *   FILE 381
//*                EXECUTING (NOT PRINTING).                        *   FILE 381
//*                                                                 *   FILE 381
//*     J005FILT - A JES2 EXIT (5) TO FILTER JES2 COMMANDS TO       *   FILE 381
//*                DISALLOW CERTAIN COMMANDS OR OPERANDS ON THE     *   FILE 381
//*                COMMANDS.                                        *   FILE 381
//*                                                                 *   FILE 381
//*     J005JIT  - A JES2 EXIT (5) TO PROVIDE A COMMAND INTERFACE   *   FILE 381
//*                TO THE JOB INFORMATION TASK THAT READS JOB       *   FILE 381
//*                DISTRIBUTION INFORMATION FROM A VSAM FILE.       *   FILE 381
//*                THIS COMMAND CAN START, STOP, RESTART, MODIFY,   *   FILE 381
//*                OR PROVIDE STATUS ABOUT THE TASK.  IT CAN ALSO   *   FILE 381
//*                LIST INDIVIDUAL RECORDS.                         *   FILE 381
//*                                                                 *   FILE 381
//*     J005LOAD - A JES2 EXIT (5) TO PROVIDE A MEANS OF RELOADING  *   FILE 381
//*                AN EXIT ROUTINE WITHOUT HAVING TO PERFORM A HOT  *   FILE 381
//*                START.                                           *   FILE 381
//*                                                                 *   FILE 381
//*     J005UCC7 - A JES2 EXIT (5) TO PROVIDE A COMMAND INTERFACE   *   FILE 381
//*                TO THE UCC7 INTERFACE TASK THAT CAN DEMAND A     *   FILE 381
//*                JOB NETWORK ON BEHALF OF THE SEPARATOR ROUTINE   *   FILE 381
//*                BASED ON INFORMATION FROM A VSAM FILE.  THIS     *   FILE 381
//*                COMMAND CAN START, STOP, RESTART, OR PROVIDE     *   FILE 381
//*                STATUS ABOUT THE TASK.                           *   FILE 381
//*                                                                 *   FILE 381
//*     J006STDS - A JES2 EXIT (6) TO PROCESS THE INTERNAL TEXT     *   FILE 381
//*                FOR ALL JOBS.  THIS ROUTINE PROVIDES ACCOUNTING  *   FILE 381
//*                VERIFICATION, ENFORCEMENT OF STANDARDS, AND      *   FILE 381
//*                SETS CLASS AND PRIORITY BASED ON THE RESOURCES   *   FILE 381
//*                REQUIRED BY A JOB.                               *   FILE 381
//*                                                                 *   FILE 381
//*     J007ENDJ - A JES2 EXIT (7) TO WRITE A SPECIAL END OF JOB    *   FILE 381
//*                MESSAGE TO THE CONSOLE (NOT THE JOB LOG).  IT    *   FILE 381
//*                IS VERY SIMILAR TO THE NORMAL END OF JOB         *   FILE 381
//*                MESSAGE EXCEPT IT INDICATES WHETHER THE JOB      *   FILE 381
//*                ABENDED OR HAD A JCL ERROR.  PRODUCTION JOBS     *   FILE 381
//*                HAVE A DIFFERENT MESSAGE NUMBER SO A WTO EXIT    *   FILE 381
//*                ROUTINE COULD MAKE ABEND AND JCL ERROR MESSAGES  *   FILE 381
//*                FOR THESE JOBS NON ROLL DELETABLE, WHICH BRINGS  *   FILE 381
//*                THESE FAILURES TO THE IMMEDIATE ATTENTION OF     *   FILE 381
//*                THE CONSOLE OPERATOR.                            *   FILE 381
//*                                                                 *   FILE 381
//*     J007JCTU - A JES2 EXIT (7) TO RETAIN THE SPECIAL USER       *   FILE 381
//*                FIELDS IN THE JQE BY COPYING THEM TO THE NJE     *   FILE 381
//*                JOB HEADER.  THIS EXIT WILL PERFORM THIS TASK    *   FILE 381
//*                EACH TIME THE JCT IS WRITTEN BACK TO THE SPOOL.  *   FILE 381
//*                THIS RETAINS THIS INFORMATION IN AN NJE          *   FILE 381
//*                ENVIRONMENT AND ACROSS A SPOOL OFFLOAD/RELOAD    *   FILE 381
//*                OPERATION.  THIS FUNCTION ALSO REQUIRES          *   FILE 381
//*                J007REST TO RESTORE THESE FIELDS AFTER A RELOAD  *   FILE 381
//*                OPERATION.                                       *   FILE 381
//*                                                                 *   FILE 381
//*     J007JQEU - A JES2 EXIT (7) TO UPDATE THE JQE USER FIELDS    *   FILE 381
//*                FROM THE AVAILABLE INFORMATION EACH TIME THE     *   FILE 381
//*                JCT IS REWRITTEN TO THE SPOOL.  THIS EXIT ALSO   *   FILE 381
//*                WRITES AN SMF TYPE 30 RECORD FOR ALL NJE PRINT   *   FILE 381
//*                JOBS TO PROVIDE ACCOUNTING INFORMATION FOR JOBS  *   FILE 381
//*                WHICH ONLY PRINT AT THIS NJE NODE.               *   FILE 381
//*                                                                 *   FILE 381
//*     J007RACF - A JES2 EXIT (7) TO RETAIN THE RACF USERID        *   FILE 381
//*                ACROSS AN NJE SYSTEM.  IBM INTENTIONALLY ZEROS   *   FILE 381
//*                OUT THE RACF FIELDS IN THE JCT PRIOR TO          *   FILE 381
//*                TRANSMISSION.  THIS FORCES JOBS TO CODE USER=    *   FILE 381
//*                AND PASSWORD= ON THE JOB CARD.  THIS EXIT        *   FILE 381
//*                RETAINS THE USERID IN A USER NJE JOB HEADER AND  *   FILE 381
//*                RESTORES IT AFTER TRANSMISSION.  THE EXIT        *   FILE 381
//*                J003UNJH IS ALSO REQUIRED FOR THIS FUNCTION TO   *   FILE 381
//*                BUILD THE USER NJE JOB HEADER.                   *   FILE 381
//*                                                                 *   FILE 381
//*     J007RLSE - A JES2 EXIT (7) TO PERFORM RELEASE PROCESSING    *   FILE 381
//*                FOR ALL JOBS THAT CONTAIN A /*RELEASE CONTROL    *   FILE 381
//*                CARD.  THIS EXIT WILL RELEASE ALL JOBS WITH THE  *   FILE 381
//*                SPECIFIED JOB NAME AND MATCHING OWNERID NAME AT  *   FILE 381
//*                END OF JOB IF THIS JOB DID NOT ABEND OR HAVE A   *   FILE 381
//*                JCL ERROR.  MESSAGES ARE WRITTEN TO THE CONSOLE  *   FILE 381
//*                GIVING THE RESULTS OF PROCESSING.                *   FILE 381
//*                                                                 *   FILE 381
//*     J011SPRT - A JES2 EXIT (11) TO PROVIDE SPOOL PARTITIONING.  *   FILE 381
//*                WHEN SPOOL VOLUMES ARE STARTED AND DRAINED TO    *   FILE 381
//*                ACCOMMODATE FLUCTUATING SPOOL REQUIREMENTS,      *   FILE 381
//*                STARTED TASKS MAY USE THE NEW SPOOL VOLUMES.     *   FILE 381
//*                THIS WILL PREVENT THAT SPOOL FROM DRAINING       *   FILE 381
//*                UNTIL THE STARTED TASK TERMINATES AND IS         *   FILE 381
//*                PURGED.  THIS EXIT PROVIDES AN ELIGIBLE LIST OF  *   FILE 381
//*                SPOOL VOLUMES FOR STARTED TASKS TO PREVENT THIS  *   FILE 381
//*                FROM OCCURRING.                                  *   FILE 381
//*                                                                 *   FILE 381
//*     J014$JSL - A JES2 EXIT (14) TO PERFORM JOB SELECTION BASED  *   FILE 381
//*                ON USER FIELDS IN THE JQE.  THIS IS WHERE THE    *   FILE 381
//*                USE OF /*THREAD AND /*EXCLUDE JECL CARDS IS      *   FILE 381
//*                PERFORMED AS WELL AS HONORING THE USER HOLD      *   FILE 381
//*                ATTRIBUTE.  BECAUSE THIS PROCESSING REQUIRES     *   FILE 381
//*                CONTROL OF THE JES2 CHECKPOINT, THESE FIELDS     *   FILE 381
//*                MUST BE IN THE JQE TO AVOID RELEASING THE        *   FILE 381
//*                CHECKPOINT.  IF THE ESOTERIC ROUTINE FACILITY    *   FILE 381
//*                IS GOING TO BE USED, USE THE EXIT 14 ROUTINE     *   FILE 381
//*                PROVIDED IN MODULE JESRESRC INSTEAD OF THIS      *   FILE 381
//*                MODULE.                                          *   FILE 381
//*                                                                 *   FILE 381
//*     J015$SP  - A JES2 EXIT (15) TO GENERATE DJDE CONTROL        *   FILE 381
//*                STATEMENTS FOR A XEROX 3700 PRINTER.  THIS       *   FILE 381
//*                EXIT REQUIRES THAT THE 9700 SUPPORT PRODUCT      *   FILE 381
//*                XJCF MARKETED BY XENOS COMPUTER SYSTEMS BE       *   FILE 381
//*                INSTALLED.                                       *   FILE 381
//*                                                                 *   FILE 381
//*     J020UHLD - A JES2 EXIT (20) TO CHANGE TYPRUN=HOLD TO A      *   FILE 381
//*                USERHOLD ATTRIBUTE.                              *   FILE 381
//*                                                                 *   FILE 381
//*     J021$57  - A JES2 EXIT (21) WHICH MODIFIES THE SMF TYPE 57  *   FILE 381
//*                RECORD WHICH RECORDS NJE ACTIVITY.  FOR SOME     *   FILE 381
//*                STRANGE REASON, THIS RECORD DOES NOT CONTAIN     *   FILE 381
//*                JOBNAME.  THE NETWORK ACCOUNTING FIELD IS        *   FILE 381
//*                OVERLAID WITH THE JOBNAME.  WHAT GOOD IS THIS    *   FILE 381
//*                INFORMATION WITHOUT BEING ABLE TO TIE IT BACK    *   FILE 381
//*                TO A JOB?                                        *   FILE 381
//*                                                                 *   FILE 381
//*     J024JIT  - A JES2 EXIT (24) WHICH STARTS THE TWO JES2 USER  *   FILE 381
//*                SUBTASKS AT INITIALIZATION TIME.  STANDARD JES2  *   FILE 381
//*                INTERFACES ARE USED TO PERFORM THIS FUNCTION.    *   FILE 381
//*                CODE IS IN THE EXITS THEMSELVES TO SHUTDOWN      *   FILE 381
//*                WHEN JES2 IS TERMINATED.  THIS EXIT REQUIRES     *   FILE 381
//*                EXIT HASPXIT0 TO ESTABLISH THE SUBTASK           *   FILE 381
//*                ENVIRONMENT.                                     *   FILE 381
//*                                                                 *   FILE 381
//*     J255$FMT - A JES2 EXIT (24) TO FORMAT JOB RELATED           *   FILE 381
//*                INFORMATION FOR A SPECIFIC JOB IN THE PASSED     *   FILE 381
//*                PARAMETER LIST.  THIS ROUTINE IS USED BY         *   FILE 381
//*                SEVERAL EXITS TO DISPLAY STATUS ABOUT A JOB.     *   FILE 381
//*                                                                 *   FILE 381
//*     HASPXIT0 - A JES2 EXIT (0) TO ALLOCATE A USER CONTROL       *   FILE 381
//*                TABLE (UCT), ALLOW THE JIT VSAM DATASET NAME TO  *   FILE 381
//*                BE SPECIFIED IN THE JES2 PARAMETERS, AND         *   FILE 381
//*                ESTABLISH THE USER WORK SELECTION FACILITY FOR   *   FILE 381
//*                FILTERING TEST AND PRODUCTION WORK ON LOCAL      *   FILE 381
//*                PRINTERS, PUNCHES, AND OFFLOAD DEVICES.          *   FILE 381
//*                                                                 *   FILE 381
//*     JESRESRC - A SERIES OF JES2 EXITS (4,5, AND 14) TO PROVIDE  *   FILE 381
//*                ESOTERIC JOB ROUTING.  THIS IS A FUNCTIONAL      *   FILE 381
//*                DUPLICATION OF THE MELLON BANK MODS TO PROVIDE   *   FILE 381
//*                THE SAME FUNCTION.  THEY WERE REWRITTEN TO FIT   *   FILE 381
//*                INTO OUR SYSTEM OF EXITS.  THE JOB SELECT EXIT   *   FILE 381
//*                14 IN THIS MODULE IS A REPLACEMENT FOR           *   FILE 381
//*                J014$JSL.  USE THIS EXIT 14 ROUTINE IF THIS      *   FILE 381
//*                FACILITY IS BEING USED OR USE THE OTHER EXIT 14  *   FILE 381
//*                ROUTINE IF ONLY IMPLEMENTING THE USER AND SETUP  *   FILE 381
//*                HOLD FACILITY.                                   *   FILE 381
//*                                                                 *   FILE 381
//*     FZ50V0   - A USERMOD TO UPDATE THE JES2 JQE AND QSE TO ADD  *   FILE 381
//*                USER FIELDS.  IT ALSO FORCES REASSEMBLY OF       *   FILE 381
//*                EVERY MODULE IN JES2 TO USE THE UPDATED MACROS.  *   FILE 381
//*                                                                 *   FILE 381
//*     FZ51V0   - A USERMOD TO ADD ALL OF THE USER MAPPING MACROS  *   FILE 381
//*                TO THE JES2 MACRO LIBRARY.  MANY OF THE EXITS    *   FILE 381
//*                REQUIRE THESE MACROS.                            *   FILE 381
//*                                                                 *   FILE 381
//*     CONSOLE  - A TSO COMMAND TO ALLOW A TSO TERMINAL TO         *   FILE 381
//*                EFFECTIVELY BE TURNED INTO A CONSOLE.  CODE      *   FILE 381
//*                WILL FUNCTION ONLY UNDER XA.  A USER SUPPLIED    *   FILE 381
//*                SVC MUST BE SUPPLIED TO GET INTO KEY ZERO FOR    *   FILE 381
//*                AUTHORIZATION PURPOSES.                          *   FILE 381
//*                                                                 *   FILE 381
//*     DSAT     - A TSO COMMAND TO RETURN DATA SET ATTRIBUTES OF   *   FILE 381
//*                DATA SETS AT A SPECIFIED INDEX LEVEL.  THIS      *   FILE 381
//*                CODE IS LOOSELY BASED ON A COMMAND FROM FPL BUT  *   FILE 381
//*                DOES NOT HAVE ALL OF THE OPTIONS.  WHAT MAKES    *   FILE 381
//*                THIS ONE DIFFERENT IS THAT IT IS WRITTEN FOR     *   FILE 381
//*                DFP ONLY AND RETURNS GDG BASE INFORMATION AS     *   FILE 381
//*                WELL AS VSAM ATTRIBUTES.                         *   FILE 381
//*                                                                 *   FILE 381
//*     TESTJES  - A PROGRAM WHICH CAN BE USED TO TEST THE SP       *   FILE 381
//*                1.3.3/1.3.4 VERSION OF JESEXIT6 BY SETTING UP A  *   FILE 381
//*                FAKE EXIT ENVIRONMENT AND THEN CALLING THE MAIN  *   FILE 381
//*                ENTRY POINT OF THE EXIT.                         *   FILE 381
//*                                                                 *   FILE 381
//*     TESTJ136 - A PROGRAM WHICH CAN BE USED TO TEST THE SP       *   FILE 381
//*                1.3.6/2.1.5 VERSION OF JESEXIT6 BY SETTING UP A  *   FILE 381
//*                FAKE EXIT ENVIRONMENT AND THEN CALLING THE MAIN  *   FILE 381
//*                ENTRY POINT OF THE EXIT.                         *   FILE 381
//*                                                                 *   FILE 381
//*     PRINTDOC - SAMPLE JCL TO PRINT THIS MEMBER ($DOC).          *   FILE 381
//*                                                                 *   FILE 381
//*                             J 0 0 6 S T D S                     *   FILE 381
//*                                                                 *   FILE 381
//*            THIS JES2 EXIT PROGRAM IS DESIGNED TO RUN AT         *   FILE 381
//*            CONVERTER TIME TO ENFORCE INSTALLATION JCL           *   FILE 381
//*            STANDARDS AND TO DETERMINE THE APPROPRIATE JOB       *   FILE 381
//*            CLASS BASED ON DEVICE UTILIZATION.                   *   FILE 381
//*                                                                 *   FILE 381
//*                    T S O    C O N S O L E    C O M M A N D      *   FILE 381
//*                                                                 *   FILE 381
//*            THIS TSO COMMAND WILL ALLOW A TSO USER TO FUNCTION   *   FILE 381
//*            AS AN O/S CONSOLE.  THE ORIGINAL CODE WAS PROBABLY   *   FILE 381
//*            THE SPY COMMAND ON THE MODS TAPES, BUT IT HAS        *   FILE 381
//*            EVOLVED OVER A PERIOD OF TIME.  I REGRET THAT THE    *   FILE 381
//*            NAME OF THE ORIGINATOR OF THE CODE HAS BEEN LOST.    *   FILE 381
//*                                                                 *   FILE 381
//*                    T S O    D S A T    C O M M A N D            *   FILE 381
//*                                                                 *   FILE 381
//*            THIS TSO COMMAND WILL ALLOW A TSO USER TO LIST DATA  *   FILE 381
//*            SET ATTRIBUTES AT A SPECIFIED INDEX LEVEL.  THE      *   FILE 381
//*            CODE IS LOOSELY BASED ON A COMMAND FROM FLORIDA      *   FILE 381
//*            POWER AND LIGHT BUT DOES NOT HAVE ALL OF THE         *   FILE 381
//*            OPTIONS.  THIS VERSION WILL WORK PROPERLY ONLY       *   FILE 381
//*            UNDER DFP USING ICF CATALOGS.  IT WILL RETURN GDG    *   FILE 381
//*            BASE INFORMATION AS WELL AS ATTRIBUTES OF VSAM DATA  *   FILE 381
//*            SETS.  THE USE OF AN UNDOCUMENTED CATALOG INTERFACE  *   FILE 381
//*            ALLOWS THIS INFORMATION TO BE OBTAINED.              *   FILE 381
//*                                                                 *   FILE 381
//*                             T E S T J 1 3 6                     *   FILE 381
//*                                                                 *   FILE 381
//*            THIS PROGRAM WAS WRITTEN TO TEST THE JES2 EXIT6      *   FILE 381
//*            PROGRAM DESIGNED TO ENFORCE INSTALLATION JCL         *   FILE 381
//*            STANDARDS AND TO SET THE APPROPRIATE JOB CLASS       *   FILE 381
//*            BASED ON DEVICES USED.                               *   FILE 381
//*                                                                 *   FILE 381
//*                             T E S T J E S                       *   FILE 381
//*                                                                 *   FILE 381
//*            THIS PROGRAM WAS WRITTEN TO TEST THE JES2 EXIT6      *   FILE 381
//*            PROGRAM DESIGNED TO ENFORCE INSTALLATION JCL         *   FILE 381
//*            STANDARDS AND TO SET THE APPROPRIATE JOB CLASS       *   FILE 381
//*            BASED ON DEVICES USED.                               *   FILE 381
//*                                                                 *   FILE 381
//*                       J E S 2    $ L F    C O M M A N D         *   FILE 381
//*                                                                 *   FILE 381
//*            A NEW COMMAND HAS BEEN ADDED TO JES2 FOR USE BY THE  *   FILE 381
//*            MVS COMPUTER CONSOLE OPERATORS.  IBM DID NOT SEE     *   FILE 381
//*            FIT TO SUPPLY AN EASY WAY FOR AN OPERATOR TO         *   FILE 381
//*            DETERMINE WHICH JOBS ARE WAITING TO PRINT, WHAT      *   FILE 381
//*            ORDER IN WHICH THESE JOBS WILL PRINT, OR HOW MANY    *   FILE 381
//*            LINES ARE TO BE PRINTED.  THE COMMAND SUPPLIED BY    *   FILE 381
//*            IBM IS THE $DF COMMAND WHICH ONLY LISTS HOW MANY     *   FILE 381
//*            JOBS ARE WAITING TO PRINT AS SEEN IN THE FOLLOWING   *   FILE 381
//*            EXAMPLE:                                             *   FILE 381
//*                                                                 *   FILE 381
//*            $DF                                                  *   FILE 381
//*            $HASP621 OUT R=LOCAL F=STD. C=****T=****W=(NONE)     *   FILE 381
//*                     CLASS A=15,R=1,C=1,D=2                      *   FILE 381
//*                                                                 *   FILE 381
//*            THIS NEW COMMAND ALLOWS THE OPERATOR TO DETERMINE    *   FILE 381
//*            THE JOBNAME, JOB NUMBER, AND NUMBER OF PRINT LINES   *   FILE 381
//*            FOR EACH PRINT GROUP.  NOTE THAT THE XS OPERAND IS   *   FILE 381
//*            OPTIONAL FOR USERS OF THE XJCF PRODUCT FROM XENOS    *   FILE 381
//*            COMPUTING WHICH GIVES NATIVE JES2 SUPPORT FOR THE    *   FILE 381
//*            XEROX 9700 PRINTER.                                  *   FILE 381
//*                                                                 *   FILE 381
//*    EXTENSIVE MODIFICATIONS HAVE BEEN MADE TO CONTROL JOB        *   FILE 381
//*    PROCESSING AT FIRST UNION NATIONAL BANK.  THIS HAS CAUSED    *   FILE 381
//*    THE ADDITION OF MANY "JOB FLAGS" TO BE ASSIGNED TO A JOB.    *   FILE 381
//*    THE STANDARD IBM DISPLAY COMMAND DOES NOT DISPLAY THESE      *   FILE 381
//*    FLAGS.  A NEW COMMAND WAS WRITTEN TO EFFECTIVELY REPLACE     *   FILE 381
//*    THE IBM $DJ OR $D'JOBNAME' COMMAND.  THE FORMAT OF THE       *   FILE 381
//*    COMMAND IS IDENTICAL TO THE IBM COMMAND EXCEPT THAT THE      *   FILE 381
//*    LETTER 'Q' IS SUBSTITUTED FOR THE LETTER 'D'.                *   FILE 381
//*                                                                 *   FILE 381
//*                           JES2 $DN COMMAND                      *   FILE 381
//*                                                                 *   FILE 381
//*    EXTENSIVE MODIFICATIONS HAVE BEEN MADE TO CONTROL JOB        *   FILE 381
//*    PROCESSING AT FIRST UNION NATIONAL BANK.  THIS HAS CAUSED    *   FILE 381
//*    THE ADDITION OF MANY "JOB FLAGS" TO BE ASSIGNED TO A JOB.    *   FILE 381
//*    THE STANDARD IBM DISPLAY COMMAND DOES NOT DISPLAY THESE      *   FILE 381
//*    FLAGS.  A NEW COMMAND WAS WRITTEN TO EFFECTIVELY REPLACE     *   FILE 381
//*    THE IBM $DN COMMAND.  THE FORMAT OF THE COMMAND IS           *   FILE 381
//*    IDENTICAL TO THE IBM COMMAND EXCEPT FOR SOME NEW ADDED       *   FILE 381
//*    PARAMETERS.  AFTER ALL SELECTED JOBS HAVE BEEN DISPLAYED,    *   FILE 381
//*    THE HASP946 MESSAGE WILL BE DISPLAYED GIVING THE PERCENT     *   FILE 381
//*    SPOOL UTILIZATION.  IF NO JOBS MEET THE DISPLAY              *   FILE 381
//*    REQUIREMENTS, ONLY THE HASP946 MESSAGE WILL BE DISPLAYED.    *   FILE 381
//*    THE IBM $DN COMMAND CAN STILL BE ACCESSED BY USING ENTERING  *   FILE 381
//*    $QN INSTEAD.                                                 *   FILE 381
//*                                                                 *   FILE 381
//*                           JES2 $TJIT COMMAND                    *   FILE 381
//*                                                                 *   FILE 381
//*    EXTENSIVE MODIFICATIONS HAVE BEEN MADE TO THE JES2 JOB       *   FILE 381
//*    SEPARATOR ROUTINES AT FIRST UNION BANK TO PROVIDE JOB        *   FILE 381
//*    DISTRITBUTION INFORMATION WHICH IS NOT NORMALLY AVAILABLE    *   FILE 381
//*    FOR A JOB.  THIS INFORMATION IS EXTRACTED FROM A VSAM FILE   *   FILE 381
//*    BY JOBNAME FOR PRODUCTION JOBS OR BY OWNERID FOR TEST JOBS.  *   FILE 381
//*    TO AVOID THE EXPOSURE OF JES2 GOING INTO A WAIT STATE WHILE  *   FILE 381
//*    READING THE VSAM FILE, THE ACTUAL I/O TO THE FILE IS         *   FILE 381
//*    PERFORMED BY A SEPARATE TASK.  ANY JES2 ROUTINE CAN REQUEST  *   FILE 381
//*    INFORMATION FROM THIS TASK BY QUEUEING A REQUEST TO THE JIT  *   FILE 381
//*    OR JOB INFORMATION TASK.  BECAUSE THE JIT IS DEPENDENT UPON  *   FILE 381
//*    BEING ABLE TO READ A VSAM FILE, THE FACILITY CAN BE          *   FILE 381
//*    EFFECTIVELY DISABLED DUE TO I/O BOTTLENECKS, I/O ERRORS, OR  *   FILE 381
//*    A DAMAGED FILE.  A MECHANISM HAS BEEN PROVIDED TO DISPLAY    *   FILE 381
//*    AND/OR ALTER THE STATUS OF THE JIT.                          *   FILE 381
//*                                                                 *   FILE 381
//*                           JES2 $TUCC7 COMMAND                   *   FILE 381
//*                                                                 *   FILE 381
//*    EXTENSIVE MODIFICATIONS HAVE BEEN MADE TO THE JES2 JOB       *   FILE 381
//*    SEPARATOR ROUTINES AT FIRST UNION BANK TO PROVIDE JOB        *   FILE 381
//*    DISTRITBUTION INFORMATION WHICH IS NOT NORMALLY AVAILABLE    *   FILE 381
//*    FOR A JOB.  THIS INFORMATION IS EXTRACTED FROM A VSAM FILE   *   FILE 381
//*    BY JOBNAME FOR PRODUCTION JOBS OR BY OWNERID FOR TEST JOBS.  *   FILE 381
//*    IF THE VSAM RECORD FOR THIS JOB REQUESTS IT, THE SEPARATOR   *   FILE 381
//*    EXIT CAN DEMAND A JOB NETWORK FROM UCC7 FOR THE JOB WHICH    *   FILE 381
//*    HAS JUST BEEN PRINTED.  THIS NETWORK MUST BE POSTED BY       *   FILE 381
//*    DISTRIBUTION WHEN THIS REPORT IS PLACED IN THE USER'S BIN    *   FILE 381
//*    OR CART.  THIS ALLOWS TRACKING OF SERVICE LEVEL AGREEMENTS   *   FILE 381
//*    FOR PRODUCTION PRINTED OUTPUT.  TO AVOID THE EXPOSURE OF     *   FILE 381
//*    JES2 GOING INTO A WAIT STATE WHILE THE UCC7 REQUEST IS       *   FILE 381
//*    BEING PROCESSED, A SEPARATE TASK HAS BEEN INITIALIZED TO     *   FILE 381
//*    PROCESS THESE REQUESTS.  ANY JES2 ROUTINE CAN DEMAND A       *   FILE 381
//*    NETWORK BY QUEUEING A REQUEST TO THE UCC7 TASK.  BECAUSE     *   FILE 381
//*    THE UCC7 INTERFACE PERFORMS EXTERNAL PROCESSING, THE         *   FILE 381
//*    FACILITY CAN BE EFFECTIVELY DISABLED DUE TO SYSTEM           *   FILE 381
//*    BOTTLENECKS. A MECHANISM HAS BEEN PROVIDED TO DISPLAY        *   FILE 381
//*    AND/OR ALTER THE STATUS OF THE UCC7 TASK.                    *   FILE 381
//*                                                                 *   FILE 381
//*                           JES2 $DV COMMAND                      *   FILE 381
//*                                                                 *   FILE 381
//*    A NEW COMMAND HAS BEEN ADDED TO JES2 FOR USE BY THE MVS      *   FILE 381
//*    COMPUTER CONSOLE OPERATORS.  THERE ARE INSTANCES WHERE       *   FILE 381
//*    SOMEONE AT THE OPERATOR CONSOLE NEETS TO DISPLAY             *   FILE 381
//*    INFORMATION ABOUT A DASD VOLUME AND ALL THAT IS KNOWN IS     *   FILE 381
//*    THE VOLSER OR VOLSER PREFIX.  THE D U,DASD,ONLINE COMMAND    *   FILE 381
//*    WAS USED TO DISPLAY ALL VOLUMES AND THE LIST SCANNED FOR     *   FILE 381
//*    THE CORRECT VOLSER.  THE $DV COMMAND GIVES THE CONSOLE       *   FILE 381
//*    OPERATOR THE ABILITY TO DISPLAY DASD VOLUMES BY VOLSER,      *   FILE 381
//*    VOLSER PREFIX, OR UNIT ADDRESS.                              *   FILE 381
//*                                                                 *   FILE 381
//*            $DV,MVSRS                                            *   FILE 381
//*            $HASP900 MVSRSG  141 3380   PRIV/RSDNT    202        *   FILE 381
//*            $HASP900 MVSRSF  250 3380   PRIV/RSDNT    000        *   FILE 381
//*            $HASP900 MVSRS2  252 3380   PRIV/RSDNT    000        *   FILE 381
//*                                                                 *   FILE 381
//*    THIS NEW COMMAND ALLOWS THE OPERATOR TO DETERMINE THE UNIT   *   FILE 381
//*    ADDRESS, DEVICE TYPE, MOUNT ATTRIBUTES, AND USE COUNT.       *   FILE 381
//*                                                                 *   FILE 381
//*                           JES2 $SL COMMAND                      *   FILE 381
//*                                                                 *   FILE 381
//*    MODIFICATIONS HAVE BEEN MADE TO THE STANDARD IBM SETUP       *   FILE 381
//*    PROCESSING AT FIRST UNION NATIONAL BANK.  WE HAVE A          *   FILE 381
//*    REQUIREMENT TO BE ABLE TO LIST ALL JOBS WHICH HAVE NOT HAD   *   FILE 381
//*    THEIR SETUP REQUIREMENTS MET.  OPERATIONS MUST ALSO BE ABLE  *   FILE 381
//*    TO RE-LIST THE JES2 SETUP CARDS WHICH DESCRIBE THE SETUP     *   FILE 381
//*    REQUIREMENTS.  THE $SL COMMAND WAS WRITTEN TO PROVIDE THIS   *   FILE 381
//*    FACILITY.                                                    *   FILE 381
//*                                                                 *   FILE 381
//*                           JES2 $SR COMMAND                      *   FILE 381
//*                                                                 *   FILE 381
//*    MODIFICATIONS HAVE BEEN MADE TO THE STANDARD IBM SETUP       *   FILE 381
//*    PROCESSING AT FIRST UNION NATIONAL BANK.  WE HAVE A          *   FILE 381
//*    REQUIREMENT TO PLACE JOBS IN A SPECIAL SETUP QUEUE UNTIL     *   FILE 381
//*    THEIR SETUP REQUIREMENTS ARE MET.  OPERATIONS MUST THEN BE   *   FILE 381
//*    ABLE SETUP THE JOB BY REMOVING THE JOB FROM THE SETUP        *   FILE 381
//*    QUEUE.  THE $SR COMMAND WAS WRITTEN TO PROVIDE THIS          *   FILE 381
//*    FACILITY.                                                    *   FILE 381
//*                                                                 *   FILE 381
//*                           JES2 $UA COMMAND                      *   FILE 381
//*                                                                 *   FILE 381
//*    MODIFICATIONS HAVE BEEN MADE TO THE STANDARD IBM HOLD        *   FILE 381
//*    PROCESSING TO PLACE JOBS IN A SPECIAL HOLD QUEUE CALLED THE  *   FILE 381
//*    USER HOLD QUEUE.  THIS IS NORMALLY ACCOMPLISHED BY USING     *   FILE 381
//*    THE TYPRUN=HOLD OPERAND ON THE JOB CARD FOR THE JOB OR       *   FILE 381
//*    USING THE HOLD OPERAND ON THE /*THREAD CARD.  THESE JOBS     *   FILE 381
//*    WILL NORMALLY BE RELEASED FROM USER HOLD BY /*RELEASE CARDS  *   FILE 381
//*    IN OTHER JOBS.  THE USER CAN ALSO RELEASE HIS/HER OWN JOBS   *   FILE 381
//*    BY ENTERING THIS COMMAND THROUGH A PROGRAMMED INTERFACE.     *   FILE 381
//*    THE $UA COMMAND WAS WRITTEN TO PROVIDE THIS FACILITY.        *   FILE 381
//*                                                                 *   FILE 381
//*                           JES2 $UH COMMAND                      *   FILE 381
//*                                                                 *   FILE 381
//*    MODIFICATIONS HAVE BEEN MADE TO THE STANDARD IBM HOLD        *   FILE 381
//*    PROCESSING TO PLACE JOBS IN A SPECIAL HOLD QUEUE CALLED THE  *   FILE 381
//*    USER HOLD QUEUE.  THIS IS NORMALLY ACCOMPLISHED BY USING     *   FILE 381
//*    THE TYPRUN=HOLD OPERAND ON THE JOB CARD FOR THE JOB OR       *   FILE 381
//*    USING THE HOLD OPERAND ON THE /*THREAD CARD.  A JOB CAN      *   FILE 381
//*    ALSO BE PLACED IN THIS QUEUE BY USING THIS COMMAND.          *   FILE 381
//*                                                                 *   FILE 381
//*                           JES2 $UL COMMAND                      *   FILE 381
//*                                                                 *   FILE 381
//*    MODIFICATIONS HAVE BEEN MADE TO THE STANDARD IBM HOLD        *   FILE 381
//*    PROCESSING TO PLACE JOBS IN A SPECIAL HOLD QUEUE CALLED THE  *   FILE 381
//*    USER HOLD QUEUE.  THIS IS NORMALLY ACCOMPLISHED BY USING     *   FILE 381
//*    THE TYPRUN=HOLD OPERAND ON THE JOB CARD FOR THE JOB OR       *   FILE 381
//*    USING THE HOLD OPERAND ON THE /*THREAD CARD.  THERE IS ALSO  *   FILE 381
//*    A REQUIREMENT TO LIST JOBS IN THIS QUEUE.                    *   FILE 381
//*                                                                 *   FILE 381
//*                           JES2 $LOAD COMMAND                    *   FILE 381
//*                                                                 *   FILE 381
//*    IN INSTALLATIONS WHICH HAVE EXTENSIVE JES2 EXIT ROUTINES,    *   FILE 381
//*    IT MAY BE HARD AT TIMES TO GET A JES2 HOT START TO RELOAD    *   FILE 381
//*    AN EXIT WHICH MUST BE MODIFIED.  HOT STARTS WORK, BUT THEY   *   FILE 381
//*    ARE VERY DISRUPTIVE TO PRINTER, RJE, AND NJE ACTIVITY.  THE  *   FILE 381
//*    $LOAD COMMAND WAS WRITTEN TO PROVIDE A FACILITY TO RELOAD A  *   FILE 381
//*    JES2 EXIT WITHOUT A JES2 OUTAGE.                             *   FILE 381
//*                                                                 *   FILE 381
//*                           JES2 $DC COMMAND                      *   FILE 381
//*                                                                 *   FILE 381
//*    THE $DC COMMAND IS ONE OF THE 4 CONSOLE COMMANDS WHICH       *   FILE 381
//*    CONTROL THE RESOURCE ROUTING FACILITY OF JES2.  THE OTHER    *   FILE 381
//*    COMMANDS ARE $QA, $QD, AND $DR.  A JOB CAN REQUEST ONE OR    *   FILE 381
//*    MORE RESOURCES FROM A PREDEFINED LIST OF RESOURCES AND WILL  *   FILE 381
//*    NOT RUN UNLESS THAT RESOURCE NAME IS ATTACHED TO THE         *   FILE 381
//*    APPROPRIATE PROCESSOR.  THIS COMMAND DISPLAYS ANY JOBS THAT  *   FILE 381
//*    CANNOT RUN BECAUSE THEY REQUEST ONE OR MORE RESOURCES THAT   *   FILE 381
//*    ARE NOT ATTACHED TO ANY PROCESSOR.  THIS COMMAND ALLOWS THE  *   FILE 381
//*    CONSOLE OPERATOR TO SEE THE CONFLICTS AND REACT              *   FILE 381
//*    APPROPRIATELY TO IT.  THIS COMMAND WILL ALSO BE INVOKED      *   FILE 381
//*    INTERNALLY WHENEVER A RESOURCE IS ADDED OR DELETED FROM A    *   FILE 381
//*    PROCESSOR.  THE FORMAT OF THE $DC COMMAND IS AS FOLLOWS:     *   FILE 381
//*                                                                 *   FILE 381
//*                           JES2 $DR COMMAND                      *   FILE 381
//*                                                                 *   FILE 381
//*    THE $DR COMMAND IS ONE OF THE 4 CONSOLE COMMANDS WHICH       *   FILE 381
//*    CONTROL THE RESOURCE ROUTING FACILITY OF JES2.  THE OTHER    *   FILE 381
//*    COMMANDS ARE $QA, $QD, AND $DC.  THIS DISPLAYS THE ESOTERIC  *   FILE 381
//*    RESOURCE NAMES THAT ARE ATTACHED TO A PROCESSOR.  A JOB      *   FILE 381
//*    THAT REQUESTS ONE OF A PREDEFINED LIST OF RESOURCES WILL     *   FILE 381
//*    NOT RUN UNLESS THAT RESOURCE NAME IS ATTACHED TO THE         *   FILE 381
//*    APPROPRIATE PROCESSOR.  THIS COMMAND ALLOWS THE CONSOLE      *   FILE 381
//*    OPERATOR TO SEE WHICH RESOURCES HAVE BEEN ATTACHED.  THIS    *   FILE 381
//*    COMMAND WILL ALSO BE INVOKED INTERNALLY WHENEVER A RESOURCE  *   FILE 381
//*    IS ADDED OR DELETED FROM A PROCESSOR.  THE FORMAT OF THE     *   FILE 381
//*    $DR COMMAND IS AS FOLLOWS:                                   *   FILE 381
//*                                                                 *   FILE 381
//*                           JES2 $QA COMMAND                      *   FILE 381
//*                                                                 *   FILE 381
//*    THE $QA COMMAND IS ONE OF THE 4 CONSOLE COMMANDS WHICH       *   FILE 381
//*    CONTROL THE RESOURCE ROUTING FACILITY OF JES2.  THE OTHER    *   FILE 381
//*    COMMANDS ARE $DR, $QD, AND $DC.  JOBS THAT REQUEST           *   FILE 381
//*    RESOURCES WILL NOT RUN UNLESS THAT RESOURCE NAME IS          *   FILE 381
//*    ATTACHED TO THE APPROPRIATE PROCESSOR.  THIS COMMAND ALLOWS  *   FILE 381
//*    THE CONSOLE OPERATOR TO ATTACH A RESOURCE NAME TO A          *   FILE 381
//*    PROCESSOR TO ALLOW THE APPROPRIATE JOBS TO RUN ON THAT       *   FILE 381
//*    MACHINE.  THE $DR COMMAND WILL BE AUTOMATICALLY INVOKED      *   FILE 381
//*    AFTER PROCESSING COMPLETES FOR THIS COMMAND TO LIST THE      *   FILE 381
//*    RESOURCES THAT ARE NOW ATTACHED.  THE $DC COMMAND WILL ALSO  *   FILE 381
//*    BE AUTOMATICALLY INVOKED TO DISPLAY ANY JOBS WHICH STILL     *   FILE 381
//*    CANNOT EXECUTE BECAUSE THE APPROPRIATE RESOURCES ARE NOT     *   FILE 381
//*    AVAILABLE.  THE FORMAT OF THE $QA COMMAND IS AS FOLLOWS:     *   FILE 381
//*                                                                 *   FILE 381
//*                           JES2 $QD COMMAND                      *   FILE 381
//*                                                                 *   FILE 381
//*    THE $QD COMMAND IS ONE OF THE 4 CONSOLE COMMANDS WHICH       *   FILE 381
//*    CONTROL THE RESOURCE ROUTING FACILITY OF JES2.  THE OTHER    *   FILE 381
//*    COMMANDS ARE $QA, $DR, AND $DC.  JOBS WHICH SPECIFY          *   FILE 381
//*    RESOURCES WILL NOT RUN UNLESS THAT RESOURCE NAME IS          *   FILE 381
//*    ATTACHED TO THE APPROPRIATE PROCESSOR.  THIS COMMAND ALLOWS  *   FILE 381
//*    THE CONSOLE OPERATOR TO DETACH A RESOURCE NAME FROM A        *   FILE 381
//*    PROCESSOR IF THAT RESOURCE IS NO LONGER AVAILABLE IN ORDER   *   FILE 381
//*    TO PREVENT JOBS WHICH REQUIRE THAT RESOURCE FROM EXECUTING.  *   FILE 381
//*    THE $DR COMMAND WILL BE AUTOMATICALLY INVOKED AFTER          *   FILE 381
//*    PROCESSING COMPLETES FOR THIS COMMAND TO LIST THE RESOURCES  *   FILE 381
//*    THAT ARE STILL ATTACHED.  THE $DC COMMAND WILL ALSO BE       *   FILE 381
//*    AUTOMATICALLY INVOKED TO DISPLAY ANY JOBS WHICH NOW CANNOT   *   FILE 381
//*    EXECUTE BECAUSE THE APPROPRIATE RESOURCES ARE NOT            *   FILE 381
//*    AVAILABLE.  THE FORMAT OF THE $QD COMMAND IS AS FOLLOWS:     *   FILE 381
//*                                                                 *   FILE 381
//*                         A U T H S V C                           *   FILE 381
//*                                                                 *   FILE 381
//*        THIS SVC IS A TYPE 4 SVC WRITTEN TO ALLOW THE            *   FILE 381
//*        CALLER TO ENTER KEY 0.  THIS SVC IS A LITTLE             *   FILE 381
//*        DIFFERENT FROM MOST OTHER SVC CODE IN THAT IT            *   FILE 381
//*        WRITES AN SMF RECORD FOR EACH CALL TO PERFORM A          *   FILE 381
//*        FUNCTION.  THE CALLING PROGRAM NAME IS ASSUMED TO        *   FILE 381
//*        BE POINTED TO BY REGISTER 0 ON INPUT AND ALL OTHER       *   FILE 381
//*        INFORMATION SUCH AS JOBNAME/TSONAME, PROGRAMMER          *   FILE 381
//*        NAME, AND ACCOUNTING INFORMATION IS EXTRACTED TO         *   FILE 381
//*        PROVIDE AN AUDIT CAPABILITY FOR UNAUTHORIZED USE.        *   FILE 381
//*        THE FUNCTION TO BE PERFORMED IS IN REGISTER 1 ON         *   FILE 381
//*        INPUT.  A ZERO INDICATES THAT PROTECT KEY ZERO IS        *   FILE 381
//*        DESIRED.  ANY OTHER VALUE WILL RESET THE USER BACK       *   FILE 381
//*        TO THE PROTECT KEY IN THE TCB.                           *   FILE 381
//*                                                                 *   FILE 381
//*                   R E S O U R C E   R O U T I N G               *   FILE 381
//*                                                                 *   FILE 381
//*        A SERIES OF EXITS AND CONTROL BLOCK MODIFICATIONS        *   FILE 381
//*        PROVIDES A FACILITY WITHIN JES2 TO ROUTE JOBS TO A       *   FILE 381
//*        RESOURCE NAME RATHER THAN A SPECIFIC PROCESSOR.          *   FILE 381
//*        THIS FACILITY IS A FUNCTIONAL COPY OF A SIMILAR          *   FILE 381
//*        FACILITY WHICH WAS DEVELOPED AND SUPPORTED BY            *   FILE 381
//*        MELLON BANK AND PROVIDED ON MANY OF THE MVS MODS         *   FILE 381
//*        TAPES.                                                   *   FILE 381
//*                                                                 *   FILE 381
```
