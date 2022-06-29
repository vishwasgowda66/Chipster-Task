# Chipster-Task
<html>

<head>
    <script src="https://code.jquery.com/jquery-3.5.1.js">
    </script>

    <style>
        .grid-item {
            background-color: white;
            border: 1px solid rgba(0, 0, 0, 0.8);
            padding: 20px;
            font-size: 30px;
            text-align: center;
        }

        #table {
            display: grid;
            grid-template-columns: auto auto auto;
            background-color: black;
            padding: 1px;
        }
    </style>
</head>

<body>
    <section>

        <div id="table">

        </div>
        <script>
            $(document).ready(function () {
                $.getJSON("data.json",
                    function (data) {
                        var user = '';
                        $.each(data, function (key, value) {
                            user += '<div class="grid-item">';
                            user += '<div>' +
                                "Name:" + value.NAME + '</div>';
                            user += '<div>' +
                                "Age:" + value.AGE + '</div>';
                            user += '</div>';
                        });

                        $('#table').append(user);
                    });
            });
        </script>
    </section>
</body>

</html>
