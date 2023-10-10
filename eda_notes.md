# Transormations	

- Rename Columns
  - columns are inconsistent and contain spelling errors.  They need to be standardized
    - 'Gender', 'Department', '10th Mark', '12th Mark', 'college mark',
      'hobbies', 'daily studing time', 'prefer to study in',
      'salary expectation', 'Do you like your degree?',
      'willingness to pursue a career based on their degree  ',
      'social medai & video', 'Travelling Time ', 'Stress Level ',
      'Financial Status', 'part-time job'
- dtypes are inconsistent. some should be converted to boolian.
  - - certification (No, Yes)
    - salary expectation
    - Do you like your degree? (No, Yes)
    - part-time job

# Data Dictionary

* `cert_course`: Indicates whether the individual has taken a certification course (Yes/No).
* `gender`: Gender of the individual.
* `dept`: Department or major.
* `mark_10th`: 10th-grade mark.
* `mark_12th`: 12th-grade mark.
* `mark_college`: College mark.
* `hobbies`: Listed hobbies.
* `study_dtime`: Daily studying time.
* `study_loc`: Preferred study location (time of day).
* `salary_expected`: Expected salary.
* `degree_satisfaction`: Satisfaction with degree (Yes/No).
* `prob_degree_career`: Probability to pursue a career based on their degree.
* `social_video_dtime`: Daily time spent on social media and video.
* `travel_dtime`: Daily travel time.
* `stress_lvl`: Stress level.
* `financial_status`: Financial status.
* `part_time_job`: Indicates whether the individual has a part-time job (True/False).
