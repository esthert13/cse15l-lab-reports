# Lab Report 3
## Introduction

In this lab report, we were to pick between the commands `less, find`, and `grep`. I chose the command `less` to expand upon, specifically on three options of it: `less -n, less -N,` and `less -X`. 

***

## `less -n`

**Example 1**
   
Input/Output: 

```
$ less -n ./technical/911report/chapter-7.txt

            THE ATTACK LOOMS
            FIRST ARRIVALS IN CALIFORNIA
            In chapter 5 we described the Southeast Asia travels of Nawaf al Hazmi, Khalid al
                Mihdhar, and others in January 2000 on the first part of the "planes operation." In
                that chapter we also described how Mihdhar was spotted in Kuala Lumpur early in
                January 2000, along with associates who were not identified, and then was lost to
                sight when the group passed through Bangkok. On January 15, Hazmi and Mihdhar
                arrived in Los Angeles. They spent about two weeks there before moving on to San
                    Diego.

            Two Weeks in Los Angeles
            Why Hazmi and Mihdhar came to California, we do not know for certain. Khalid Sheikh
                Mohammed (KSM), the organizer of the planes operation, explains that California was
                a convenient point of entry from Asia and had the added benefit of being far away
                from the intended target area.

            Hazmi and Mihdhar were ill-prepared for a mission in the United States. Their only
                qualifications for this plot were their devotion to Usama Bin Ladin, their veteran
                service, and their ability to get valid U.S. visas. Neither had spent any
                substantial time in the West, and neither spoke much, if any, English.

            It would therefore be plausible that they or KSM would have tried to identify, in
                advance, a friendly contact for them in the United States. In detention, KSM denies
                that al Qaeda had any agents in Southern California. We do not credit this
                denial.4We believe it is unlikely that Hazmi and Mihdhar-neither of whom, in
                contrast to the Hamburg group, had any prior exposure to life in the West-would have
                come to the United States without arranging to receive assistance from one or more
                individuals informed in advance of their arrival.

            KSM says that though he told others involved in the conspiracy to stay away from
                mosques and to avoid establishing personal contacts, he made an exception in this
                case and instructed Hazmi and Mihdhar to pose as newly arrived Saudi students and
                seek assistance at local mosques. He counted on their breaking off any such
                relationships once they moved to the East Coast.

            Our inability to ascertain the activities of Hazmi and Mihdhar during their first two
```

**Example 2**

Input/Output:

```
$ less -n ./technical/government/Alcohol_Problems/Session2-PDF.txt

Session 2.
Identifying ED Patients with Alcohol Problems

Robert Woolard, MD
Many patients in the emergency department (ED) have alcohol
problems, and they can be identified.1 Research on techniques used
to identify these patients has been conducted, but several areas of
interest should be addressed by further research. We need to
further examine and refine alcohol-screening questionnaires in the
ED. We need to determine the sequence and combination of questions
and tests that constitute the best screening process. We need to
study barriers to screening, identify factors that promote
screening implementation, and demonstrate the impact of a screening
program in the ED. The final aim of screening must be improved
outcomes through referral and counseling. Identification is only
the first step in a process of care.
Alcohol problems defined
Alcohol problems designate a spectrum from risk behavior to
illness, and from problematic consumption to alcohol use disorder.
We must be careful when interpreting the results of studies, and in
our own design of screening procedures, that we are clear about the
endpoints we are measuring. Clinicians in the ED are interested in
screening for several alcohol endpoints. Acute intoxication is of
concern to emergency physicians. Intoxication in a driver would
certainly be considered an "alcohol problem." The blood or breath
alcohol concentration (BAC), coupled with our clinical
observations, may help us identify intoxication. Most alcohol
screening tests identify patients with alcohol use disorders or
problematic consumption of alcohol. The American Psychiatric
Association in DSM III-R, IV2 and the World Health Organization
(WHO) in the 9th and 10th International Classification of Diseases
(ICD-9, -10) have rigorously defined alcohol abuse and alcohol
dependence.3 These definitions largely agree for dependence, but
not for abuse. DSM includes social and legal consequences of abuse
and ICD-10 has only medical and psychological consequences. Fewer
```

**Example 3**

Input/Output:

```
$ less -n ./technical/government/Env_Prot_Agen/atx1-6.txt

Methods for Measuring the Acute Toxicity of Effluents and
Receiving Waters to Freshwater and Marine Organisms
Fifth Edition
October 2002



U.S. Environmental Protection AgencyOffice of Water (4303T)
1200 Pennsylvania Avenue, NW Washington, DC 20460
EPA-821-R-02-012
The Engineering and Analysis Division, of the Office of Science
and Technology, has reviewed and approved this report for
publication. Neither the United States Government nor any of its
employees, contractors, or their employees make any warranty,
expressed or implied, or assumes any legal liability or
responsibility for any third party's use of or the results of such
use of any information, apparatus, product, or process discussed in
this report, or represents that its use by such party would not
infringe on privately owned rights.

INTRODUCTION
```

**Explanation and Potential Usage**

`less -n` removes line numbers from text, as seen in the examples above. This is very useful if you ever want to print solely the contents of a text file for formatting purposes.

***

## `less -N`

**Example 1**
   
Input/Output: 

```
$ less -N ./technical/911report/chapter-7.txt

      1
      2
      3
      4             THE ATTACK LOOMS
      5             FIRST ARRIVALS IN CALIFORNIA
      6             In chapter 5 we described the Southeast Asia travels of Nawaf al Hazmi, Khalid al
      7                 Mihdhar, and others in January 2000 on the first part of the "planes operation." In
      8                 that chapter we also described how Mihdhar was spotted in Kuala Lumpur early in
      9                 January 2000, along with associates who were not identified, and then was lost to
     10                 sight when the group passed through Bangkok. On January 15, Hazmi and Mihdhar
     11                 arrived in Los Angeles. They spent about two weeks there before moving on to San
     12                     Diego.
     13
     14             Two Weeks in Los Angeles
     15             Why Hazmi and Mihdhar came to California, we do not know for certain. Khalid Sheikh
     16                 Mohammed (KSM), the organizer of the planes operation, explains that California was
     17                 a convenient point of entry from Asia and had the added benefit of being far away
     18                 from the intended target area.
     19
     20             Hazmi and Mihdhar were ill-prepared for a mission in the United States. Their only
     21                 qualifications for this plot were their devotion to Usama Bin Ladin, their veteran
     22                 service, and their ability to get valid U.S. visas. Neither had spent any
     23                 substantial time in the West, and neither spoke much, if any, English.
```

**Example 2**

Input/Output:

```
$ less -N ./technical/government/Alcohol_Problems/Session2-PDF.txt

      1
      2
      3
      4
      5 Session 2.
      6 Identifying ED Patients with Alcohol Problems
      7
      8 Robert Woolard, MD
      9 Many patients in the emergency department (ED) have alcohol
     10 problems, and they can be identified.1 Research on techniques used
     11 to identify these patients has been conducted, but several areas of
     12 interest should be addressed by further research. We need to
     13 further examine and refine alcohol-screening questionnaires in the
     14 ED. We need to determine the sequence and combination of questions
     15 and tests that constitute the best screening process. We need to
     16 study barriers to screening, identify factors that promote
     17 screening implementation, and demonstrate the impact of a screening
     18 program in the ED. The final aim of screening must be improved
     19 outcomes through referral and counseling. Identification is only
     20 the first step in a process of care.
     21 Alcohol problems defined
     22 Alcohol problems designate a spectrum from risk behavior to
     23 illness, and from problematic consumption to alcohol use disorder.
     24 We must be careful when interpreting the results of studies, and in
     25 our own design of screening procedures, that we are clear about the
     26 endpoints we are measuring. Clinicians in the ED are interested in
     27 screening for several alcohol endpoints. Acute intoxication is of
     28 concern to emergency physicians. Intoxication in a driver would
     29 certainly be considered an "alcohol problem." The blood or breath
     30 alcohol concentration (BAC), coupled with our clinical
     31 observations, may help us identify intoxication. Most alcohol
     32 screening tests identify patients with alcohol use disorders or
     33 problematic consumption of alcohol. The American Psychiatric
     34 Association in DSM III-R, IV2 and the World Health Organization
     35 (WHO) in the 9th and 10th International Classification of Diseases
     36 (ICD-9, -10) have rigorously defined alcohol abuse and alcohol
     37 dependence.3 These definitions largely agree for dependence, but
     38 not for abuse. DSM includes social and legal consequences of abuse
     39 and ICD-10 has only medical and psychological consequences. Fewer
```

**Example 3**

Input/Output:

```
$ less -N ./technical/government/Env_Prot_Agen/atx1-6.txt

      1
      2
      3
      4
      5 Methods for Measuring the Acute Toxicity of Effluents and
      6 Receiving Waters to Freshwater and Marine Organisms
      7 Fifth Edition
      8 October 2002
      9
     10
     11
     12 U.S. Environmental Protection AgencyOffice of Water (4303T)
     13 1200 Pennsylvania Avenue, NW Washington, DC 20460
     14 EPA-821-R-02-012
     15 The Engineering and Analysis Division, of the Office of Science
     16 and Technology, has reviewed and approved this report for
     17 publication. Neither the United States Government nor any of its
     18 employees, contractors, or their employees make any warranty,
     19 expressed or implied, or assumes any legal liability or
     20 responsibility for any third party's use of or the results of such
     21 use of any information, apparatus, product, or process discussed in
     22 this report, or represents that its use by such party would not
     23 infringe on privately owned rights.
     24
     25 INTRODUCTION
     26
```

**Explanation and Potential Usage**

`less -N` adds line numbers to text, as seen in the examples above. This is very useful if you ever want to print the contents of a text file with line numbers for easier referencing of specific lines and/or pure formatting purposes.

***

## `less -X`

**Example 1**
   
Input/Output: 

```
$ less -X ./technical/911report/chapter-7.txt

            THE ATTACK LOOMS
            FIRST ARRIVALS IN CALIFORNIA
            In chapter 5 we described the Southeast Asia travels of Nawaf al Hazmi, Khalid al      
                Mihdhar, and others in January 2000 on the first part of the "planes operation." In
                that chapter we also described how Mihdhar was spotted in Kuala Lumpur early in    
                January 2000, along with associates who were not identified, and then was lost to  
                sight when the group passed through Bangkok. On January 15, Hazmi and Mihdhar      
                arrived in Los Angeles. They spent about two weeks there before moving on to San   
                    Diego.

            Two Weeks in Los Angeles
            Why Hazmi and Mihdhar came to California, we do not know for certain. Khalid Sheikh    
                Mohammed (KSM), the organizer of the planes operation, explains that California was
                a convenient point of entry from Asia and had the added benefit of being far away  
                from the intended target area.

            Hazmi and Mihdhar were ill-prepared for a mission in the United States. Their only
                qualifications for this plot were their devotion to Usama Bin Ladin, their veteran
                service, and their ability to get valid U.S. visas. Neither had spent any
                substantial time in the West, and neither spoke much, if any, English.

            It would therefore be plausible that they or KSM would have tried to identify, in
                advance, a friendly contact for them in the United States. In detention, KSM denies
                that al Qaeda had any agents in Southern California. We do not credit this
                denial.4We believe it is unlikely that Hazmi and Mihdhar-neither of whom, in
                contrast to the Hamburg group, had any prior exposure to life in the West-would have
                come to the United States without arranging to receive assistance from one or more
                individuals informed in advance of their arrival.

            KSM says that though he told others involved in the conspiracy to stay away from
                mosques and to avoid establishing personal contacts, he made an exception in this
                case and instructed Hazmi and Mihdhar to pose as newly arrived Saudi students and
                seek assistance at local mosques. He counted on their breaking off any such
[cs15lfa22mi@ieng6-201]:skill-demo1:142$ 
```

**Example 2**

Input/Output:

```
$ less -X ./technical/government/Alcohol_Problems/Session2-PDF.txt

Session 2.
Identifying ED Patients with Alcohol Problems

Robert Woolard, MD
Many patients in the emergency department (ED) have alcohol        
problems, and they can be identified.1 Research on techniques used 
to identify these patients has been conducted, but several areas of
interest should be addressed by further research. We need to       
further examine and refine alcohol-screening questionnaires in the 
ED. We need to determine the sequence and combination of questions 
and tests that constitute the best screening process. We need to   
study barriers to screening, identify factors that promote
screening implementation, and demonstrate the impact of a screening
program in the ED. The final aim of screening must be improved     
outcomes through referral and counseling. Identification is only   
the first step in a process of care.
Alcohol problems defined
Alcohol problems designate a spectrum from risk behavior to        
illness, and from problematic consumption to alcohol use disorder. 
We must be careful when interpreting the results of studies, and in
our own design of screening procedures, that we are clear about the
endpoints we are measuring. Clinicians in the ED are interested in 
screening for several alcohol endpoints. Acute intoxication is of  
concern to emergency physicians. Intoxication in a driver would
certainly be considered an "alcohol problem." The blood or breath
alcohol concentration (BAC), coupled with our clinical
observations, may help us identify intoxication. Most alcohol
screening tests identify patients with alcohol use disorders or
problematic consumption of alcohol. The American Psychiatric
Association in DSM III-R, IV2 and the World Health Organization
(WHO) in the 9th and 10th International Classification of Diseases
(ICD-9, -10) have rigorously defined alcohol abuse and alcohol
dependence.3 These definitions largely agree for dependence, but
not for abuse. DSM includes social and legal consequences of abuse
and ICD-10 has only medical and psychological consequences. Fewer
[cs15lfa22mi@ieng6-201]:skill-demo1:147$
```

**Example 3**

Input/Output:

```
$ less -X ./technical/government/Env_Prot_Agen/atx1-6.txt

Methods for Measuring the Acute Toxicity of Effluents and
Receiving Waters to Freshwater and Marine Organisms
Fifth Edition
October 2002



U.S. Environmental Protection AgencyOffice of Water (4303T)        
1200 Pennsylvania Avenue, NW Washington, DC 20460
EPA-821-R-02-012
The Engineering and Analysis Division, of the Office of Science    
and Technology, has reviewed and approved this report for
publication. Neither the United States Government nor any of its   
employees, contractors, or their employees make any warranty,      
expressed or implied, or assumes any legal liability or
responsibility for any third party's use of or the results of such 
use of any information, apparatus, product, or process discussed in
this report, or represents that its use by such party would not    
infringe on privately owned rights.

INTRODUCTION

[cs15lfa22mi@ieng6-201]:skill-demo1:151$ 
```

**Explanation and Potential Usage**

`less -X` disables clearing the terminal screen when quitting `less`, as seen in the examples above. Generally, when quitting `less`, the contents of the file disappear; this command prevents it from doing so. This is very useful if you ever want to keep the contents of the file in the terminal even when you exit for maybe comparing two different files or with/without line numbers.


End.


