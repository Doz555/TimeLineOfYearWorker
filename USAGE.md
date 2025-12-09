# Usage Guide - Timeline of Year

## Quick Start (เริ่มต้นอย่างรวดเร็ว)

### 1. Open the Timeline
Simply double-click on either `2.html` or `3.html` to open in your web browser. No installation needed!

### 2. View Your Projects
The timeline will automatically load all projects from `data.csv` and display them organized by department.

### 3. Understand the Layout
- **Header** - Shows report title and description
- **Color Bands** - Each color represents a different department
- **Dates** - Shows project start and end dates
- **Project Names** - Thai language project descriptions

---

## Understanding the Display

### Department Colors Explained

When viewing the timeline, each colored section represents a different department:

| Color | Department | Type |
|-------|-----------|------|
| 🔵 Blue | HK (Human Resources) | Company management, meetings, budgets |
| 🟢 Green | IT (Information Technology) | System updates, bug fixes, support |
| 🟡 Yellow | APP (Application) | Mobile app development, UI/UX design |
| 🔴 Red | PAS (Purchase & Supply) | Procurement, vendor agreements |
| 🟣 Purple | HT_Report (Sales Report) | Sales forecasting, revenue reports |

### Timeline Information

Each project shows:
- **Project Name** - Description in Thai language
- **Start Date** - When the project begins
- **End Date** - When the project is completed
- **Duration** - How long the project takes (shown by position on timeline)

---

## Managing Project Data

### Adding a New Project

1. Open `data.csv` with a text editor (Notepad, VS Code, etc.)
2. Go to the end of the file
3. Add a new line with this format:
   ```
   DEPARTMENT,Project Description,YYYY/MM/DD,YYYY/MM/DD
   ```

### Example:
```
IT,แก้ไข Bug ระบบลงทะเบียน,2025/04/15,2025/04/20
APP,ออกแบบหน้า Dashboard,2025/04/16,2025/04/25
HK,ประชุมคณะกรรมการ ครั้งที่ 3,2025/04/28,2025/04/28
```

### Editing Existing Projects

1. Open `data.csv`
2. Find the project line you want to edit
3. Modify the department, name, or dates
4. Save the file
5. Refresh the HTML file in your browser

### Deleting a Project

1. Open `data.csv`
2. Find the project line
3. Delete the entire line
4. Save the file
5. Refresh the browser

---

## Department Selection

### How to Choose the Right Department

When adding a project, select the appropriate department code:

#### HK - Human Resources (ฝ่ายทรัพยากรบุคคล)
- Company meetings
- Team building activities
- Annual planning
- Budget preparation
- Training and development

**Example:**
```
HK,ประชุมประจำปี 2025 และวางแผนกลยุทธ์,2025/01/01,2025/01/01
HK,กิจกรรมสร้างทีม (Team Building),2025/04/04,2025/04/04
HK,จัดทำแผนงบประมาณประจำปี 2026,2025/03/17,2025/03/21
```

#### IT - Information Technology (ฝ่าย IT)
- System upgrades
- Bug fixes and hotfixes
- IT support and maintenance
- Security audits
- Server administration

**Example:**
```
IT,รายงาน IT Support แยกหัวข้อแจ้งปัญหา,2025/01/02,2025/01/02
IT,อัพเกรดระบบปฏิบัติการ Server หลัก,2025/02/10,2025/02/14
IT,แก้ไข Bug Critical ในระบบแจ้งปัญหา,2025/03/03,2025/03/03
```

#### APP - Application Development (ฝ่าย Development)
- Mobile app development
- UI/UX design
- Feature development
- User testing (UAT)
- Beta releases

**Example:**
```
APP,ออกแบบ Mockup สำหรับ Mobile App,2025/01/09,2025/01/10
APP,เริ่มพัฒนา Feature A,2025/02/04,2025/02/07
APP,ทดสอบ Beta Version ของ Mobile App,2025/03/05,2025/03/12
```

#### PAS - Purchase & Supply Chain (ฝ่าย Purchasing)
- Vendor negotiations
- Supply chain management
- Procurement processes
- Supplier agreements
- Policy reviews

**Example:**
```
PAS,ทบทวนและปรับปรุงขั้นตอนการอนุมัติโปรเจกต์,2025/01/06,2025/01/08
PAS,อบรมการใช้ระบบ ERP ใหม่,2025/02/17,2025/02/17
PAS,เจรจาสัญญากับ Supplier รายใหม่,2025/03/14,2025/03/14
```

#### HT_Report - Sales Report (ฝ่าย Business)
- Sales reporting
- Revenue forecasting
- Business analysis
- Quarterly reports
- Sales summaries

**Example:**
```
HT_Report,สรุปยอดขายรายวันและจัดทำรายงาน,2025/01/13,2025/01/13
HT_Report,จัดทำรายงานพยากรณ์ไตรมาส 2/2025,2025/02/24,2025/02/26
```

---

## Date Format

### Important: Date Format is YYYY/MM/DD

Always use this exact format:
- **Year**: 4 digits (e.g., 2025)
- **Month**: 2 digits (e.g., 01 for January, 12 for December)
- **Day**: 2 digits (e.g., 05, 15, 28)

### Examples:
- ✅ `2025/01/15` - Correct
- ✅ `2025/12/31` - Correct
- ❌ `01/15/2025` - Wrong format
- ❌ `2025-01-15` - Wrong separator (use / not -)
- ❌ `2025/1/5` - Missing leading zeros

### Single-Day Projects

If a project completes on the same day it starts, use the same date twice:
```
HK,ประชุมประจำปี 2025,2025/01/01,2025/01/01
```

### Multi-Day Projects

Projects can span multiple days:
```
APP,เริ่มพัฒนา Feature A,2025/02/04,2025/02/07
```

This shows a 4-day project from February 4-7, 2025.

---

## Viewing Tips

### Best Practices

1. **Regular Updates** - Update the CSV file regularly to keep timeline current
2. **Descriptive Names** - Use clear project descriptions so others understand
3. **Realistic Dates** - Set achievable start and end dates
4. **Consistent Departments** - Use the same department codes throughout

### Filtering Tips

- Look for specific colors to find department-specific projects
- Scan the timeline to identify busy periods
- Check for overlapping projects to manage workload

### Responsive Viewing

The timeline adapts to different screen sizes:
- **Desktop** - Full width display with all details
- **Tablet** - Adjusted layout for smaller screens
- **Mobile** - Stacked layout for easy viewing

---

## Common Tasks

### Task: Add Q2 Projects

1. Open `data.csv`
2. Collect Q2 dates (April, May, June 2025)
3. Add entries like:
```
IT,อัพเดท Security Patch,2025/04/05,2025/04/10
APP,ทดสอบ Feature B,2025/04/12,2025/04/25
HK,ประชุมความก้าวหน้า Q2,2025/05/15,2025/05/15
```

### Task: Update a Project Duration

1. Open `data.csv`
2. Find the project line
3. Change the end date to the new completion date
4. Save and refresh

Example change:
```
Before: APP,พัฒนา Feature C,2025/03/15,2025/03/20
After:  APP,พัฒนา Feature C,2025/03/15,2025/03/28
```

### Task: Mark Project as Complete

1. Set the end date to today or completion date
2. The project will appear as completed on the timeline

### Task: Move Project to Different Department

1. Open `data.csv`
2. Change the department code in the first column
3. Save and refresh

Example:
```
Before: IT,แก้ไข Bug,2025/04/01,2025/04/05
After:  APP,แก้ไข Bug,2025/04/01,2025/04/05
```

---

## Troubleshooting Common Issues

### Issue: Projects Not Showing Up

**Solution:**
1. Check that `data.csv` is in the same folder as the HTML files
2. Open your browser's developer console (F12)
3. Look for error messages
4. Verify CSV format is correct
5. Try refreshing the page (Ctrl+R or Cmd+R)

### Issue: Dates Showing as "Invalid"

**Solution:**
1. Check date format is `YYYY/MM/DD`
2. Verify month is 01-12
3. Verify day is 01-31 (appropriate for the month)
4. Don't use hyphens (-), only forward slashes (/)

### Issue: Department Colors Not Showing

**Solution:**
1. Check department code spelling (HK, IT, APP, PAS, HT_Report)
2. Department codes are case-sensitive
3. Try refreshing the page
4. Clear browser cache if needed

### Issue: Thai Text Not Displaying

**Solution:**
1. Make sure your `data.csv` is saved as UTF-8 encoding
2. Check browser's font settings
3. Try using a different web browser
4. Verify Google Fonts (Sarabun) is loading properly

---

## Tips for Effective Timeline Management

1. **Keep It Updated** - Update CSV weekly or bi-weekly
2. **Be Realistic** - Set achievable deadlines
3. **Communicate Changes** - Notify team if deadlines shift
4. **Group Related Tasks** - Consider multi-day projects for related work
5. **Review Regularly** - Check the timeline in team meetings
6. **Archive Old Data** - Keep completed projects for reference but consider archiving

---

## File Backup

It's important to backup your `data.csv` regularly:

1. **Create Backups**
   - Copy `data.csv` and rename to `data_backup_2025-01-01.csv`
   - Store in a safe location

2. **Version Control**
   - Use Git to track changes
   - Commit when making significant updates
   - Can revert to previous versions if needed

---

## Support

If you encounter issues:

1. Check this guide first
2. Review the DOCUMENTATION.md file
3. Check browser console for errors (F12)
4. Verify all file paths are correct
5. Try a different web browser

---

## Summary Checklist

- [ ] Open HTML file in web browser
- [ ] See timeline populated with projects
- [ ] Understand color-coded departments
- [ ] Can read project dates and names
- [ ] Know how to edit `data.csv`
- [ ] Can add new projects
- [ ] Can update existing projects
- [ ] Know correct date format (YYYY/MM/DD)
- [ ] Understand department codes
- [ ] Have backed up your data

---

**Happy timeline tracking! 📅✨**
