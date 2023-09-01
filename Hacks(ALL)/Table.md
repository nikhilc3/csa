---
layout: default
title: Table
type: hacks
courses: { 'csa': {'week':2} } 
---

<!-- Head contains information to Support the Document -->
<head>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        h2 {
            text-align: center;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        th {
            background-color: #f2f2f2;
        }
        th, td {
            padding: 10px;
            text-align: center;
            border: 1px solid #ddd;
        }
        tr:hover {
            background-color: #f5f5f5;
        }
    </style>
    <!-- load jQuery and DataTables output style and scripts -->
    <link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/1.13.4/css/jquery.dataTables.min.css">
    <script type="text/javascript" language="javascript" src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script>var define = null;</script>
    <script type="text/javascript" language="javascript" src="https://cdn.datatables.net/1.13.4/js/jquery.dataTables.min.js"></script>
</head>

<!-- Body contains the contents of the Document -->
<body>
    <table id="demo" class="table">
        <thead>
            <tr>
                <th>Planet</th>
                <th>Distance from Sun (AU)</th>
                <th>Mass (Earth Masses)</th>
                <th>Moons</th>
                <th>Orbit Period (Earth Days)</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Mercury</td>
                <td>0.39</td>
                <td>0.055</td>
                <td>0</td>
                <td>88</td>
            </tr>
            <tr>
                <td>Venus</td>
                <td>0.72</td>
                <td>0.815</td>
                <td>0</td>
                <td>225</td>
            </tr>
            <tr>
                <td>Earth</td>
                <td>1</td>
                <td>1</td>
                <td>1</td>
                <td>365.25</td>
            </tr>
            <tr>
                <td>Mars</td>
                <td>1.52</td>
                <td>0.107</td>
                <td>2</td>
                <td>687</td>
            </tr>
            <tr>
                <td>Jupiter</td>
                <td>5.20</td>
                <td>318</td>
                <td>79</td>
                <td>4333</td>
            </tr>
            <tr>
                <td>Saturn</td>
                <td>9.58</td>
                <td>95.2</td>
                <td>82</td>
                <td>10759</td>
            </tr>
            <tr>
                <td>Uranus</td>
                <td>19.2</td>
                <td>14.5</td>
                <td>27</td>
                <td>30687</td>
            </tr>
            <tr>
                <td>Neptune</td>
                <td>30.1</td>
                <td>17.2</td>
                <td>14</td>
                <td>60190</td>
            </tr>
        </tbody>
    </table>
</body>

<!-- Script is used to embed executable code -->
<script>
    $("#demo").DataTable();
</script>
