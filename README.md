# RTO Attendance Dashboard

A browser-based reporting tool that shows whether teams are meeting their return-to-office policy, and whether people who book a desk actually come in.

**Live demo:** https://akshayvishwanath-cmd.github.io/rto-attendance-dashboard/
Open it and click **Use sample data** to explore with synthetic employees.

## The problem

Return-to-office policies raise questions every week. Who met their required office days? Which departments and managers fall short? Do the people who book seats turn up? The answers sit in separate exports (a Power BI report, attendance files, seat bookings, the employee list and leave records) that don't line up on their own. I built this to show a team what that reporting could look like.

## What I built

- **Load the data you already have:** a Power BI `.pbix` file (its data model is read in the browser), or weekly and daily attendance CSVs, plus seat bookings, employee info and leave.
- **Fair targets:** required days adjust for public holidays and each person's leave, with a configurable weekly policy.
- **Views for each role:** admin, department head and manager, with the manager view following the reporting hierarchy.
- **Adherence reporting:** office presence by week, department, org unit and employee, plus people in office by date.
- **Bookings vs attendance:** booked vs attended by date, by hierarchy and by employee.
- **Data checks:** a Data tab shows what was loaded, which columns were matched, and rows that didn't fit (duplicates, people missing from the employee file, off-domain accounts).

## Product decisions

- **Everything runs in the browser.** Files are read locally and never uploaded, so HR data stays on the user's machine.
- **Accept messy real exports.** Columns are matched by common names, and dates are parsed from several formats, so teams don't have to reformat files first.
- **Show the checks.** Reporting on attendance affects people, so the tool shows exactly which rows it counted and which it dropped.

## Result

- Demoed to stakeholders as a pitch for the reporting.
- Tested with real export files.
- Shaped a product decision.

## Built with

Claude Code and Claude chat · React · JSZip and a WebAssembly decoder for `.pbix` files · plain CSV parsing

## Run it locally

Download `index.html` and open it in a browser. It needs an internet connection to load React from a CDN.

---

Part of my product portfolio.
