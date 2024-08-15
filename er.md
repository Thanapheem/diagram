```mermaid
erDiagram
applicants ||--|{positions: has
applicants }|--|{ ranking: has
positions }|--|| ranking: ""
applicants {
number applicant_id PK "auto increment"
string fname   "Apple"
string lname   "Papaya"
string phone_number "099999999"
string position_id FK"auto increment"
string email "abc@gmail.com"
string status "Called"
string source "platform jobsdb or jobtopgun"
string edu_institution "สถานศึกษา"
string edu_faculty "คณะ"
string edu_major "สาขา"
float gpa "3.15"
string graduated_year "2022"
json work_experience ""
datetime created_at  "10-11-2022"
}
positions {
number position_id PK "auto increment"
string postion_name "Business Analyst"
string job_descriptions "ASDFGH"
json skill ""
}
ranking {
number rank_id PK "auto increment"
number applicant_id FK "auto increment"
number matching_score "44%"
number suggest_score "78%"
number suggest_position "Software Engineer"
}
```
