
<!DOCTYPE html>
<html>
<head>
  <title>My First Website</title>
</head>
<body>
  <h1>Hello 👋 I'm Sushan</h1>
  <p>Welcome to my first website hosted on GitHub Pages!</p>
</body>
</html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Attendance Tracker</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: #f4f6f9;
      text-align: center;
    }
    header {
      background: #0073e6;
      color: white;
      padding: 20px;
    }
    table {
      margin: 20px auto;
      border-collapse: collapse;
      width: 80%;
    }
    th, td {
      border: 1px solid #ddd;
      padding: 10px;
    }
    th {
      background: #0073e6;
      color: white;
    }
    tr:nth-child(even) {
      background: #f2f2f2;
    }
    button {
      padding: 8px 12px;
      margin: 5px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    .present { background: #28a745; color: white; }
    .absent { background: #dc3545; color: white; }
    .reset { background: #ffc107; color: black; }
  </style>
</head>
<body>
  <header>
    <h1>📊 Attendance Tracker</h1>
    <p>Mark students as Present ✅ or Absent ❌</p>
  </header>

  <table>
    <thead>
      <tr>
        <th>Student Name</th>
        <th>Status</th>
        <th>Action</th>
      </tr>
    </thead>
    <tbody id="attendanceTable">
      <tr>
        <td>Sushan</td>
        <td id="status1">Not Marked</td>
        <td>
          <button class="present" onclick="markAttendance('status1','Present')">Present</button>
          <button class="absent" onclick="markAttendance('status1','Absent')">Absent</button>
        </td>
      </tr>
      <tr>
        <td>Pavan</td>
        <td id="status2">Not Marked</td>
        <td>
          <button class="present" onclick="markAttendance('status2','Present')">Present</button>
          <button class="absent" onclick="markAttendance('status2','Absent')">Absent</button>
        </td>
      </tr>
      <tr>
        <td>Sreesanth</td>
        <td id="status3">Not Marked</td>
        <td>
          <button class="present" onclick="markAttendance('status3','Present')">Present</button>
          <button class="absent" onclick="markAttendance('status3','Absent')">Absent</button>
        </td>
      </tr>
    </tbody>
  </table>

  <button class="reset" onclick="resetAttendance()">Reset All</button>

  <script>
    function markAttendance(id, status) {
      document.getElementById(id).innerText = status;
    }

    function resetAttendance() {
      let cells = document.querySelectorAll("tbody td[id]");
      cells.forEach(cell => cell.innerText = "Not Marked");
    }
  </script>
</body>
</html>

