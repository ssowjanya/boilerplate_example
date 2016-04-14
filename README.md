# boilerplate_example
$(function() {

    var entries = [];
    var url = "http://jsonplaceholder.typicode.com/users?callback=?";

    $.getJSON(url, function (data) {
        $.each(data, function (i, f) {
            var tblRow = "<tr>" + "<td>" + f.id + "</td>" + "<td>" + f.name + "</td>" + "<td>"+f.username+ "</td>" + "<td> " + f.email + "</td>"  + "<td> " + f.address.street + "</td>" + "<td> " + f.address.city + "</td>"  + "<td> " + f.address.zipcode + "</td>" +"<td> " + f.address.geo.lat + "</td>" + "</tr>"
            $(tblRow).appendTo("#entrydata tbody");
        });

    });
});


<html>
<head>

</head>

<body>

<div class="wrapper">
        <table id= "entrydata" class="table table-bordered table-striped" >
            <thead>

            <th>ID</th>
            <th>Name</th>
            <th>UserName</th>
            <th>Email</th>
            <th>Street</th>
            <th>City</th>
            <th>Zipcode</th>
            <th>latitude</th>
            </thead>
            <tbody>

            </tbody>
        </table>

    </div>

<link rel="stylesheet" href="http://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.0/jquery.min.js"></script>
<script src="http://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js"></script>
<script src="js/data.js"></script>
</body>

</html>
