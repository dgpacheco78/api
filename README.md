<h1>API</h1>

https://jsonplaceholder.typicode.com/

    <html lang="es">

    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta http-equiv="X-UA-Compatible" content="ie=edge">
        <title>Consumo de API "jsonplaceholder"</title>
    </head>

    <body>
        <p>
            <div class="container">
                <h2>{JSON} Placeholder</h2>
                    <div id="data">
                    </div>
            </div>
        </p>

        <script>
            let url = 'https://jsonplaceholder.typicode.com/users/';    //Fetch toma un argumento 
            fetch(url)                                                  //(la ruta del recurso que quieres obtener)
                .then(response => response.json())                      //y devuelve un objeto Promise conteniendo 
                .then(data => mostrarData(data))                        //la respuesta, un objeto Response.
            //El objeto Response es enviado a la funcion mostrarData
            //a traves del arreglo "data"

            const mostrarData = (data) => {                             //La funcion mostrarData toma como parametro
                console.log(data);                                      //el arreglo "data"
                let body = "";
                console.log(data[1].name);
                console.log(data.length);
                /*
                for (let i = 0; i < data.length; i++) {                  //El ciclo for recorre el arreglo obteniendo
                    //todos los elementos y concatenandolos en la cadena "body"
                    body += `${data[i].id} ${data[i].name} ${data[i].username} ${data[i].email} ${data[i].address.street} <br>`;
                }
                document.getElementById('data').innerHTML = body;       //La cadena "body" es escrita en el id="data" del html 
                */
            }
        </script>

    </body>

    </html>


