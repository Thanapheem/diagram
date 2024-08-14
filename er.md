```mermaid
erDiagram
applicants ||--|{positions: has
applicants }|--|{ ranking: has
positions }|--|| ranking: ""
applicants {
number id pk "auto increment"
string name   "Full name"
string phone_number 
string position_id 
string source "platform jobsdb or jobtopgun"
string edu_institution "สถานศึกษา"
string edu_faculty "คณะ"
string edu_major "สาขา" 
float gpa
string graduated_year ""
number work_experience 
datetime created_at  
}
positions {
number id
string postion_name
string job_descriptions
json skill
}
ranking {
number id
number applicant_id
number matching_score
number suggest_score
number suggest_position
}
```
