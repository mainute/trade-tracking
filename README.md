
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trading Track Dashboard</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f2f5;
        }
        .sidebar {
            width: 250px;
            background-color: #343a40;
            color: #fff;
            height: 100vh;
            position: fixed;
            top: 0;
            left: 0;
            display: flex;
            flex-direction: column;
            padding: 20px;
        }
        .sidebar a {
            color: #ccc;
            text-decoration: none;
            padding: 10px 15px;
            border-radius: 5px;
            margin-bottom: 10px;
            display: block;
        }
        .sidebar a:hover,
        .sidebar a.active {
            background-color: #495057;
            color: #fff;
        }
        .main-content {
            margin-left: 270px;
            padding: 20px;
        }
        .section {
            display: none;
        }
        .section.active {
            display: block;
        }
        h1 {
            margin-bottom: 20px;
        }
        .card {
            background: #fff;
            border: 1px solid #ddd;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            padding: 20px;
            margin-bottom: 20px;
        }
        .card h3 {
            margin-top: 0;
        }
    </style>
</head>
<body>
    <div class="sidebar">
        <h2>Trading Track</h2>
        <a href="#overview" class="menu-link active" onclick="showSection('overview')">Overview</a>
        <a href="#analytics" class="menu-link" onclick="showSection('analytics')">Analytics</a>
        <a href="#settings" class="menu-link" onclick="showSection('settings')">Settings</a>
    </div>
    <div class="main-content">
        <!-- Overview Section -->
        <div id="overview" class="section active">
            <h1>Overview</h1>
            <div class="card">
                <h3>Account Summary</h3>
                <p>Total Trades: 120</p>
                <p>Winning Trades: 75</p>
                <p>Losing Trades: 45</p>
            </div>
        </div>

        <!-- Analytics Section -->
        <div id="analytics" class="section">
            <h1>Analytics</h1>
            <div class="card">
                <h3>Performance Chart</h3>
                <p>Placeholder for analytics charts (e.g., trade performance over time).</p>
            </div>
        </div>

        <!-- Settings Section -->
        <div id="settings" class="section">
            <h1>Settings</h1>
            <div class="card">
                <h3>Profile Settings</h3>
                <p>Update your email, password, and preferences here.</p>
            </div>
        </div>
    </div>

    <script>
        // JavaScript to handle navigation and section display
        function showSection(sectionId) {
            // Hide all sections
            document.querySelectorAll('.section').forEach((section) => {
                section.classList.remove('active');
            });

            // Remove 'active' class from all menu links
            document.querySelectorAll('.menu-link').forEach((link) => {
                link.classList.remove('active');
            });

            // Show the selected section and highlight the active menu link
            document.getElementById(sectionId).classList.add('active');
            document.querySelector(`a[href="#${sectionId}"]`).classList.add('active');
        }
    </script>
</body>
</html>
# trade-tracking
