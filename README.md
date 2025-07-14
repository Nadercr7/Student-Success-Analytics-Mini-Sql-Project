
# 🎓 Student Success Analytics – Mini Project

**As part of my Data Analysis Internship with NTI** (National Telecommunication Institute)

---

## 📌 About the Project

This project aims to explore and analyze a dataset designed to support AI-driven education management systems in higher education. It includes **student demographics, academic performance, LMS behavioral engagement**, and **risk labels** for early intervention.

---

## 📂 Dataset Features

The dataset includes:

* 🎓 **Student Demographics**: age, gender, major
* 📚 **Academic Records**: GPA, course load, attendance
* 💻 **LMS Engagement**: logins, video completion, forum activity
* ⚠️ **Risk Labels**: Low / Medium / High

---

## 🧠 Questions Explored

* Does **attendance** really predict risk level?
* Are **younger students** more likely to struggle?
* Does **forum participation** and **LMS activity** correlate with student success?
* Which **majors** have higher dropout or leave rates?
* Are there **quiet high-performers** who need different kinds of support?

---

## 🧮 Tools & Skills

* SQL (for data extraction and analysis)
* Excel / Google Sheets (for visualization)
* PowerPoint (for storytelling & presentation)

---

## 📊 Sample SQL Queries

```sql
-- Average attendance by risk level
SELECT 
    risk_level,
    AVG(attendance_rate) AS avg_attendance
FROM students
GROUP BY risk_level;
```

```sql
-- Forum participation grouping and risk
SELECT 
    CASE 
        WHEN forum_participation_count < 3 THEN 'Low'
        ELSE 'Active'
    END AS participation,
    risk_level,
    COUNT(*) AS student_count
FROM students
GROUP BY participation, risk_level;
```

---

## 📈 Key Insights

* 📉 Low attendance and low forum activity strongly correlate with higher risk.
* 🧒 Students under 20 are at the highest risk.
* 🧩 Some students have high GPA but zero engagement — a potential blind spot.
* 🏫 Engineering and CS majors have more students leaving than graduating.

---

## 📝 Final Thought

Academic success is multi-dimensional.
Combining behavioral and academic data gives us a more complete picture — helping advisors and institutions support **all students**, not just those who ask for help.

---

> ✅ Created by: **Nader Mohamed**
> 🔗 Connect with me on [LinkedIn](https://www.linkedin.com/in/nadermohamed7/)
