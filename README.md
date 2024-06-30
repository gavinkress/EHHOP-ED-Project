#  
<head>
    <meta charset="UTF-8">
    <meta content="width=device-width, initial-scale=1.0" name="viewport">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" rel="stylesheet">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600&display=swap');
        body {
            font-family: 'Open Sans', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f6f8;
            color: #333;
        }
        header {
            background-color: #FFFFFF;
            color: #000;
            padding: 20px 0;
            text-align: center;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
        }
        header img {
            width: 100px;
            vertical-align: middle;
            margin-right: 20px;
        }
        header h1 {
            font-size: 1.8em;
            color: #2a3f54;
        }
        nav {
            display: flex;
            justify-content: center;
            background-color: #00aaff;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        nav a {
            color: #fff;
            padding: 14px 20px;
            text-decoration: none;
            text-transform: uppercase;
            transition: background 0.3s ease;
        }
        nav a:hover {
            background-color: #0088cc;
        }
        .container {
            max-width: 1000px;
            margin: 40px auto;
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .hero-image {
            width: 100%;
            height: auto;
        }
        .info, .qa {
            margin-top: 40px;
        }
        .info h2, .qa h2 {
            color: #00aaff;
            border-bottom: 2px solid #00aaff;
            padding-bottom: 10px;
        }
        .info p, .qa p {
            font-size: 1em;
            line-height: 1.6;
        }
        .collapsible {
            background-color: #00aaff;
            color: white;
            cursor: pointer;
            padding: 10px;
            width: 100%;
            border: none;
            text-align: left;
            outline: none;
            font-size: 1em;
            transition: background 0.3s ease;
        }
        .collapsible:hover {
            background-color: #0088cc;
        }
        .collapsible:after {
            content: '\002B';
            font-size: 1.5em;
            color: white;
            float: right;
            margin-left: 5px;
        }
        .content {
            padding: 0 18px;
            display: none;
            overflow: hidden;
            background-color: #f1f1f1;
        }
        .contact {
            margin-top: 40px;
            padding: 20px;
            background-color: #f4f6f8;
            border: 1px solid #ddd;
        }
        .contact h2 {
            color: #00aaff;
            border-bottom: 2px solid #00aaff;
            padding-bottom: 10px;
        }
        .contact table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 10px;
        }
        .contact th, .contact td {
            padding: 10px;
            text-align: left;
            border-bottom: 1px solid #ddd;
            transition: background 0.3s ease;
        }
        .contact th:hover, .contact td:hover {
            background-color: #f1f1f1;
        }
        footer {
            text-align: center;
            padding: 10px 0;
            background-color: #333;
            color: #fff;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
        .icon {
            margin-right: 8px;
        }
    </style>
</head>
<body>
<header>
    <img alt="Logo" src="https://upload.wikimedia.org/wikipedia/en/thumb/9/94/ISMMS.svg/156px-ISMMS.svg.png">
    <h1>Icahn School of Medicine at Mount Sinai<br>EHHOP ED Project</h1>
</header>
<nav>
    <a href="#info"><i class="fas fa-info-circle icon"></i>About</a>
    <a href="#qa"><i class="fas fa-question-circle icon"></i>Q & A</a>
    <a href="#contact"><i class="fas fa-envelope icon"></i>Contact</a>
</nav>
<div class="container">
    <img alt="EHHOP ED Project" class="hero-image" src="https://images.squarespace-cdn.com/content/5efcdc780ccf5b7f5d08a77b/1593709284045-PAIQHCI1Q2QW798U9YXF/EHHOP_LOG.jpg?format=1500w&content-type=image%2Fjpeg">
    <div class="info" id="info">
        <h2>Analysis Information</h2>
        <p>About Icahn School of Medicine at Mount Sinai's EHHOP Analysis and methods.</p>
    </div>
    <div class="qa" id="qa">
        <h2>Q & A</h2>
        <button class="collapsible" type="button">Example Question 1</button>
        <div class="content">
            <p>Example Answer 1</p>
        </div>
        <button class="collapsible" type="button">Example Question 2</button>
        <div class="content">
            <p>Example Answer 2</p>
        </div>
        <button class="collapsible" type="button">Example Question 3</button>
        <div class="content">
            <p>Example Answer 3</p>
        </div>
    </div>
    <div class="contact" id="contact">
        <h2>Contact Us</h2>
        <table>
            <tr>
                <th>Name</th>
                <th>Email</th>
            </tr>
            <tr>
                <td>Gavin Kress</td>
                <td><a href="mailto:gavin.kress@icahn.mssm.edu">gavin.kress@icahn.mssm.edu</a></td>
            </tr>
            <tr>
                <td>Haley Yettman</td>
                <td><a href="mailto:support@example.com">support@example.com</a></td>
            </tr>
            <!-- Add more contacts as needed -->
        </table>
    </div>

</div>
<footer>
    &copy; 2024 ISMMS EHHOP. All rights reserved.
</footer>
<script>
    document.addEventListener('DOMContentLoaded', function () {
        var coll = document.getElementsByClassName("collapsible");
        for (var i = 0; i < coll.length; i++) {
            coll[i].addEventListener("click", function () {
                this.classList.toggle("active");
                var content = this.nextElementSibling;
                if (content.style.display === "block") {
                    content.style.display = "none";
                } else {
                    content.style.display = "block";
                }
            });
        }
    });
</script>
</body>
