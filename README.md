~~~~~~~~~~~~~~~~

//***FILE 078 IS FROM JOHN KALINICH OF THE U.S. ARMY IN ST LOUIS,   *   FILE 078
//*           MISSOURI, WITH ONE ADDITION FROM LIONEL DYCK OF       *   FILE 078
//*           KAISER PERMANENTE IN WALNUT CREEK, CA.  THIS FILE     *   FILE 078
//*           CONTAINS A COLLECTION OF ISPF EDIT MACROS AND OTHER   *   FILE 078
//*           ISPF GOODIES.  THIS FILE COMES FROM JOHN AND          *   FILE 078
//*           LIONEL'S ISPF FILES ON THE SHARE CD ROM (SHARE        *   FILE 078
//*           85 CURRENTLY), BUT JOHN PREPARED THIS VERSION FOR     *   FILE 078
//*           CBT TAPE DISTRIBUTION SPECIFICALLY.                   *   FILE 078
//*                                                                 *   FILE 078
//*      ISPF Edit Macros & Dialogs                                 *   FILE 078
//*      July 16, 1998                                              *   FILE 078
//*                                                                 *   FILE 078
//*             John Kalinich                                       *   FILE 078
//*             USA Logistics Systems                               *   FILE 078
//*              Support Center                                     *   FILE 078
//*             AMSEL-SE-BSD-LS-TD, Room 7.103                      *   FILE 078
//*             1222 Spruce Street                                  *   FILE 078
//*             St. Louis, MO.  63103-2834                          *   FILE 078
//*                                                                 *   FILE 078
//*             314-331-4521                                        *   FILE 078
//*             314-331-4520 (FAX)                                  *   FILE 078
//*                                                                 *   FILE 078
//*     SHARE Installation Code:  ALM                               *   FILE 078
//*     Internet mailbox:  jkalinic@csc.com                         *   FILE 078
//*                                                                 *   FILE 078
//*    .------------------------------------------------------.     *   FILE 078
//*    |     Feel free to call if you have any problems       |     *   FILE 078
//*    |       with this code.                                |     *   FILE 078
//*    |     If you can't reach me by phone, then send me     |     *   FILE 078
//*    |       an e-mail or fax.                              |     *   FILE 078
//*    '------------------------------------------------------'     *   FILE 078
//*                                                                 *   FILE 078
//*     File     Ext    Description                                 *   FILE 078
//*                                                                 *   FILE 078
//*     $CHANGE  LOG    Changes to macros/dialogs since SHARE 78    *   FILE 078
//*     $INSTALL ME     An attempt at install instructions          *   FILE 078
//*     $READ    ME     What you are reading                        *   FILE 078
//*     $WARRAN  TEE    The standard "mods" disclaimer              *   FILE 078
//*     #ACFCOMP PAN    Tutorial panel for ACFCOMP macro            *   FILE 078
//*     #ACFTRAP PAN    Tutorial panel for ACFTRAP macro            *   FILE 078
//*     #ASA2PC  PAN    Tutorial panel for ASA2PC macro             *   FILE 078
//*     #BROWSE4 PAN    Tutorial panel for BROWSE4 macro            *   FILE 078
//*     #EOL     PAN    Tutorial panel for EOL macro                *   FILE 078
//*     #FX      PAN    Tutorial panel for FX macro                 *   FILE 078
//*     #FXC     PAN    Tutorial panel for FXC macro                *   FILE 078
//*     #GO      PAN    Tutorial panel for GO macro                 *   FILE 078
//*     #JC      PAN    Tutorial panel for JC macro                 *   FILE 078
//*     #LISTDSI PAN    Tutorial panel for LISTDSI macro            *   FILE 078
//*     #MEMLIST PAN    Tutorial panel for MEMLIST macro            *   FILE 078
//*     #OPER    PAN    Tutorial panel for OPER macro               *   FILE 078
//*     #PLUG    PAN    Tutorial panel for PLUG macro               *   FILE 078
//*     #PROFSET PAN    Tutorial panel for PROFSET macro            *   FILE 078
//*     #RUN     PAN    Tutorial panel for RUN macro                *   FILE 078
//*     #RUNACF  PAN    Tutorial panel for RUNACF macro             *   FILE 078
//*     #SHOWCUT PAN    Tutorial panel for SHOWCUT macro            *   FILE 078
//*     #TESTACF PAN    Tutorial panel for TESTACF macro            *   FILE 078
//*     #UNX     PAN    Tutorial panel for UNX macro                *   FILE 078
//*     #WEAVE   PAN    Tutorial panel for WEAVE macro              *   FILE 078
//*     ACFCOMP  REX    ACFCOMP macro - Compile the ACF2 rule       *   FILE 078
//*                     currently being edited                      *   FILE 078
//*     ACFTRAP  REX    ACFTRAP macro - Queue ACF subcommands and   *   FILE 078
//*                     trap output                                 *   FILE 078
//*     ASA2PC   REX    ASA2PC macro - Convert ASA printer control  *   FILE 078
//*                     to ASCII code                               *   FILE 078
//*     BROWSE4  CLI    BROWSE4 macro - Invoke ISPF Browse/View     *   FILE 078
//*                     while in edit                               *   FILE 078
//*     BROWZE   CLI    CLIST dialog to browse data sets (for ISPF  *   FILE 078
//*                     command table usage)                        *   FILE 078
//*     CALCP    PAN    Pop-up window used in CALC                  *   FILE 078
//*                     command/COMPUTE dialog                      *   FILE 078
//*     CEILING  REX    REXX function to find smallest integer      *   FILE 078
//*                     >= argument                                 *   FILE 078
//*     CLONEID  REX    REXX dialog to decomp a logonid into        *   FILE 078
//*                     INSERT format for cloning                   *   FILE 078
//*     COMPUTE  REX    REXX dialog to calculate Rexx               *   FILE 078
//*                     arithmetic expressions                      *   FILE 078
//*     DSK33XX  CLI    CLIST dialog for disk space calculation     *   FILE 078
//*                     (3350/3380/3390)                            *   FILE 078
//*     DSK33XX  PAN    ISPF panel for disk space calculation       *   FILE 078
//*                     (3350/3380/3390)                            *   FILE 078
//*     DVOL     CLI    CLIST dialog to display disk free space     *   FILE 078
//*                     stats from DVOL command                     *   FILE 078
//*     DVOL     PAN    ISPF panel for DVOL dialog                  *   FILE 078
//*     DVOLTBLH PAN    Tutorial panel for DVOL table display       *   FILE 078
//*                     (short)                                     *   FILE 078
//*     DVOLTBLL PAN    ISPF panel used by DVOL table display       *   FILE 078
//*                     (long)                                      *   FILE 078
//*     DVOLTBLS PAN    ISPF panel used by DVOL table display       *   FILE 078
//*                     (short)                                     *   FILE 078
//*     EB       CLI    CLIST dialog to Edit/Browse by the          *   FILE 078
//*                     numbers from a menu of DSNs                 *   FILE 078
//*     EBH01A   PAN    Tutorial panel for Edit/Browse menu         *   FILE 078
//*     EBH01B   PAN    Turorial panel for Edit/Browse set          *   FILE 078
//*                     default modes and libraries                 *   FILE 078
//*     EB00     MSG    ISPF messages for Edit/Browse dialog        *   FILE 078
//*     EB01A    PAN    ISPF panel for Edit/Browse menu             *   FILE 078
//*     EB01B    PAN    ISPF panel for Edit/Browse set default      *   FILE 078
//*                     modes and libraries                         *   FILE 078
//*     EDET     CLI    CLIST dialog to edit data sets (for         *   FILE 078
//*                     ISPF command table usage)                   *   FILE 078
//*     EDITALL  REX    Run an ISPF Edit macro against every        *   FILE 078
//*                     member of a PDS.  (from Lionel Dyck)        *   FILE 078
//*     EOL      REX    EOL macro - Set cursor at end of            *   FILE 078
//*                     current screen line                         *   FILE 078
//*     FLOOR    REX    REXX function to find largest integer       *   FILE 078
//*                     <= argument                                 *   FILE 078
//*     FX       CLI    FX macro  - FIND 'str' ALL                  *   FILE 078
//*                     after EXCLUDE ALL                           *   FILE 078
//*     FX       SPF    FX macro  - REXX version for SPF/PC         *   FILE 078
//*                     Version 3.0                                 *   FILE 078
//*     FXC      CLI    FXC macro - FIND 'str @ cursor' ALL         *   FILE 078
//*                     after EXCLUDE ALL                           *   FILE 078
//*     GETACCT  REX    REXX sub-function to get accounting         *   FILE 078
//*                     info from ACT                               *   FILE 078
//*     GETACF2  REX    REXX sub-function to get ACF2 release       *   FILE 078
//*                     identifier from ACCVT                       *   FILE 078
//*     GETATTR  REX    REXX sub-function to get TSO user           *   FILE 078
//*                     attributes from PSCB                        *   FILE 078
//*     GETCIB   REX    REXX sub-function to get command verb       *   FILE 078
//*                     code from 1st CIB                           *   FILE 078
//*     GETCPUM  REX    REXX sub-function to get CPU model          *   FILE 078
//*                     from CVT prefix                             *   FILE 078
//*     GETDEST  REX    REXX sub-function to get TSO SYSOUT         *   FILE 078
//*                     destination from PSCB                       *   FILE 078
//*     GETDFPL  REX    REXX sub-function to get DFP level          *   FILE 078
//*                     from DFA                                    *   FILE 078
//*     GETGRPN  REX    REXX sub-function to get group              *   FILE 078
//*                     connect name from ACEE                      *   FILE 078
//*     GETIPLD  REX    REXX sub-function to get IPL date           *   FILE 078
//*                     from SMCA                                   *   FILE 078
//*     GETIPLT  REX    REXX sub-function to get IPL time           *   FILE 078
//*                     from SMCA                                   *   FILE 078
//*     GETJES2  REX    REXX sub-function to get JES2 product       *   FILE 078
//*                     name from HASPSSSM                          *   FILE 078
//*     GETJOBID REX    REXX sub-function to get JES2 job id        *   FILE 078
//*                     from SSIB                                   *   FILE 078
//*     GETLPAR  REX    REXX sub-function to get LPAR mode          *   FILE 078
//*                     from SCCB                                   *   FILE 078
//*     GETNAME  REX    REXX sub-function to get user name          *   FILE 078
//*                     from ACEE                                   *   FILE 078
//*     GETPLEX  REX    REXX sub-function to get SYSPLEX name       *   FILE 078
//*                     from ECVT                                   *   FILE 078
//*     GETPRGNM REX    REXX sub-function to get programmer         *   FILE 078
//*                     name from ACT                               *   FILE 078
//*     GETREALM REX    REXX sub-function to get real memory        *   FILE 078
//*                     size at IPL                                 *   FILE 078
//*     GETREGK  REX    REXX sub-function to get region size        *   FILE 078
//*                     from LDA                                    *   FILE 078
//*     GETSCPN  REX    REXX sub-function to get MVS SCP name       *   FILE 078
//*                     from CVT prefix                             *   FILE 078
//*     GETSMFID REX    REXX sub-function to get smfid              *   FILE 078
//*                     from SMCA                                   *   FILE 078
//*     GETSMS   REX    REXX sub-function to get SMS status         *   FILE 078
//*                     from JESCTEXT                               *   FILE 078
//*     GETSWA   REX    REXX sub-function to get location of        *   FILE 078
//*                     SWA from JCT                                *   FILE 078
//*     GETTRID  REX    REXX sub-function to get terminal id        *   FILE 078
//*                     from ACEE                                   *   FILE 078
//*     GETUID   REX    REXX sub-function to get ACF2 userid        *   FILE 078
//*                     string                                      *   FILE 078
//*     GO       CLI    GO macro - SUBMIT job then invoke IOF       *   FILE 078
//*     IDCAMS   REX    IDCAMS macro - execute IDCAMS commands      *   FILE 078
//*                     (like =3.2.V 'exec')                        *   FILE 078
//*     IEBUPDTE BAT    DOS batch file #2 to consolidate            *   FILE 078
//*                     members for upload to MVS                   *   FILE 078
//*     INFO     ABC    Action bar choice panel code to             *   FILE 078
//*                     display system information                  *   FILE 078
//*     ISFP     CLI    World's shortest CLIST                      *   FILE 078
//*     ISFPANEL PAN    SDSF panel modifications for OPER macro     *   FILE 078
//*     ISPCMDS  TBL    ISPF commands to be added to ISPCMDS        *   FILE 078
//*                     for dialog invocation                       *   FILE 078
//*     ISR@PRIM PAN    ISPF Primary Option Menu (Version 3.3)      *   FILE 078
//*     ISRUTIL  PAN    ISPF (Version 2.3) utility panel            *   FILE 078
//*                     modifications for =3.14B                    *   FILE 078
//*     ISRZ00   MSG    ISPF messages ISRZ000W and ISRZ001W         *   FILE 078
//*                     displayed in windows                        *   FILE 078
//*     JC       CLI    JC macro - JOB card generator               *   FILE 078
//*     JC       PAN    ISPF panel used by JC and JCI macros        *   FILE 078
//*     JCI      CLI    JCI macro - JOB card generator (for         *   FILE 078
//*                     use after file tailoring)                   *   FILE 078
//*     LIBDIR   REX    REXX exec to display a CA-Librarian         *   FILE 078
//*                     index                                       *   FILE 078
//*     LISTDSI  CLI    LISTDSI macro - List dataset info in        *   FILE 078
//*                     OPT32 format                                *   FILE 078
//*     LOGLIST  CLI    CLIST dialog to define output               *   FILE 078
//*                     descriptors for ISPLOG/ISPLIST              *   FILE 078
//*     LOGLIST  JCL    ISPF skeleton used by LOGLIST dialog        *   FILE 078
//*     LOGLIST  PAN    ISPF panel used by LOGLIST dialog           *   FILE 078
//*     MEMLIST  CLI    MEMLIST macro - Display member list         *   FILE 078
//*                     of PDS on =NOTE= lines                      *   FILE 078
//*     MVS      BAS    MVS basica program - Pseudo-display         *   FILE 078
//*                     of ISPF Primary Option Menu                 *   FILE 078
//*     NOWARN   REX    REXX exec that issues RECOVERY OFF          *   FILE 078
//*                     NOWARN (used with PROFSET)                  *   FILE 078
//*     OPER     CLI    OPER macro - Issued canned operator         *   FILE 078
//*                     commands via SDSF                           *   FILE 078
//*     PDSDIR   REX    REXX exec to display a PDS directory        *   FILE 078
//*     PDSFTP   PAN    ISPF pop-up panel used by PDSFTP dialog     *   FILE 078
//*     PDSFTP   REX    REXX dialog to automate PDS member FTP's    *   FILE 078
//*     PDSFTPLM PAN    ISPF member list panel used by PDSFTP       *   FILE 078
//*     PDSFTPT  PAN    Tutorial panel for PDSFTP                   *   FILE 078
//*     PLUG     REX    PLUG macro - Plug data into a range         *   FILE 078
//*                     of lines at a given column                  *   FILE 078
//*     PLUG     SPF    PLUG macro - REXX version for SPF/PC        *   FILE 078
//*                     Version 3.0                                 *   FILE 078
//*     PROFSET  REX    PROFSET macro - Mass change all edit        *   FILE 078
//*                     profiles for an applid                      *   FILE 078
//*     RESETID  REX    REXX exec to reduce ACF2 password           *   FILE 078
//*                     violation count by 1                        *   FILE 078
//*     RUN      CLI    RUN macro - EXECute the CLIST/EXEC          *   FILE 078
//*                     that is being edited                        *   FILE 078
//*     RUNACF   REX    RUNACF macro - Issue ACF subcommands        *   FILE 078
//*                     currently being edited                      *   FILE 078
//*     SHOWCUT  CLI    SHOWCUT macro - Browse the ISPF CUT         *   FILE 078
//*                     table(s) - PDS 8.5 CUT                      *   FILE 078
//*     SHOWCUTP PAN    ISPF panel used by SHOWCUT table            *   FILE 078
//*                     display                                     *   FILE 078
//*     SORTWORK PAN    ISPF panel used by SORTWORK dialog          *   FILE 078
//*     SORTWORK REX    REXX dialog to calculate SYNCSORT           *   FILE 078
//*                     sortwork space                              *   FILE 078
//*     STARTUP  CLI    CLIST code run during TSO start-up to       *   FILE 078
//*                     execute @LOGLIST                            *   FILE 078
//*     SUPERC   CLI    CLIST dialog for SEARCH-FOR batch job       *   FILE 078
//*                     (OPT314B)                                   *   FILE 078
//*     SUPERC   JCL    ISPF skeleton JCL to invoke SUPERC          *   FILE 078
//*                     program in batch                            *   FILE 078
//*     SYSLOG   CLI    CLIST dialog for browsing of current        *   FILE 078
//*                     or previous SYSLOG                          *   FILE 078
//*     SYSLOG   PAN    ISPF panel used by SYSLOG dialog            *   FILE 078
//*     TESTACF  REX    TESTACF macro - Test ACF2 rules based       *   FILE 078
//*                     on DSN= values in JCL                       *   FILE 078
//*     TRAPCMD  REX    REXX dialog to trap TSO/REXX output         *   FILE 078
//*                     and display in ISPF table                   *   FILE 078
//*     TRAPTBL  PAN    ISPF panel used by TRAPCMD table            *   FILE 078
//*                     display                                     *   FILE 078
//*     TRICMDS  PAN    Tutorial panel for ISPF command help        *   FILE 078
//*     TRIJOBS  PAN    ISPF panel used to display key jobs         *   FILE 078
//*                     with SDSF or IOF                            *   FILE 078
//*     TRIMACS  PAN    Tutorial panel for edit macro help          *   FILE 078
//*     UNX      CLI    UNX macro - Show the first n line(s)        *   FILE 078
//*                     from each X-cluded block                    *   FILE 078
//*     UPLOAD   BAT    DOS batch file #1 to consolidate            *   FILE 078
//*                     members for upload to MVS                   *   FILE 078
//*     WEAVE    REX    WEAVE macro - Interlace CUT table           *   FILE 078
//*                     into a range of lines                       *   FILE 078
//*                                                                 *   FILE 078
~~~~~~~~~~~~~~~~

