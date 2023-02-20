# KhaiClient
Client for https://education.khai.edu to get schedule.

## How to use?

First of all, you must initialize the client:
```cs
var client = new KhaiClient();
```

After that you can get a schedule for a student, lecturer, or room as follow:
```cs
var studentSchedule  = await client.GetStudentWeekSheduleAsync("student-id");
var lecturerSchedule = await client.GetLecturerWeekSheduleAsync("lekturer-id");
var groupSchedule    = await client.GetGroupWeekSheduleAsync("group-id");
```

## How to get IDs?

When you select student/lecturer/room on the [website](https://education.khai.edu/union/schedule/student), the URL is changed. The last part of the URL is the ID that you need.