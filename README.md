# CUHK Course Parser
### Functions
* `search_subject`: Input desired subject code, e.g. ACCT, parser will save courses under ACCT in `dirname/ACCT.json`.

* `parse_all`: Parses all subjects, and save courses in `subject.json` for each subject.

### Example
```python
cusis = Course(dirname='courses')
cusis.search_subject('AIST')
```
In `courses/AIST.json` (Selected)

```json
[
   {
      "code":"3020",
      "title":"Introduction to Computer Systems",
      "career":"Undergraduate",
      "units":"3.00",
      "grading":"Graded",
      "components":"Laboratory Lecture",
      "campus":"Main Campus",
      "academic_group":"Dept of Computer Sci & Engg",
      "requirements":"Prerequisite: (ENGG1110 or ESTR1002) AND (ENGG2440 or ESTR2004)",
      "description":"This course aims to provide students the basic knowledge of computer systems through the study of computer organization, assembly language and C programming. The course will mainly have two parts: (1) the structure of a computer that includes topics like data representations, digital logic structures, the Von Neumann model, assembly language, I/O, traps, subroutines and the stack; (2) system programming with C that includes topics like functions, pointers and arrays, file operations, dynamic memory management and data structures.",
      "outcome":"At the end of the course of studies, students will have acquired the ability to\r\u00a01. understand the underlying structure of a computer, the functions of its components, and the Von Neumann model;\u00a02. write simple assembly programs and understand how assembly programs works;\u00a03. develop system-level software with C.",
      "syllabus":"This course aims to provide students the basic knowledge of computer systems through the study of computer organization, assembly language and C programming. The course will mainly have two parts: (1) the structure of a computer that includes topics like data representations, digital logic structures, the Von Neumann model, assembly language, I/O, traps, subroutines and the stack; (2) system programming with C that includes topics like functions, pointers and arrays, file operations, dynamic memory management and data structures.",
      "required_readings":"1. Introduction to Computing Systems: From Bits and Gates to C and Beyond, Yale Patt and Sanjay Patel\r\u00a02. Computer systems: a programmer\u2019s perspective, Randal E. Bryant, David R. O\u2019Hallaron",
      "recommended_readings":"",
      "terms":{
         "2020-21 Term 2":{
            "--LEC (5034)":{
               "startTimes":[
                  "11:30",
                  "16:30"
               ],
               "endTimes":[
                  "12:15",
                  "18:15"
               ],
               "days":[
                  2,
                  3
               ],
               "locations":[
                  "Online Teaching",
                  "Online Teaching"
               ],
               "instructors":[
                  "Professor xxx",
                  "Professor xxx"
               ]
            },
            "-L01-LAB (5035)":{
               "startTimes":[
                  "16:30"
               ],
               "endTimes":[
                  "17:15"
               ],
               "days":[
                  2
               ],
               "locations":[
                  "Online Teaching"
               ],
               "instructors":[
                  "Professor xxx"
               ]
            }
         }
      },
      "assessments":{
         "Essay test or exam":"40",
         "Homework or assignment":"40",
         "Lab reports":"10",
         "Others":"10"
      }
   }
]
```

### How to Use
Modify the main function in `course.py` and run it.

You need to enter a captcha (Opened in a new window) for every subject you want to parse.

Output:
```
Parsing courses under subject AIST
Input the captcha here: 9P22
Found 10 courses under subject AIST
Posting request #x for AIST1000 Introduction to Artificial Intelligence and Machine Learning
Saved 10 AIST courses in courses/AIST.json
```

### Todo
1. Auto captcha
2. Replace special chars in fields like outcome and syllabus with something normal
