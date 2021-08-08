#api_events
API Rest que permite crear usuarios, iniciar sesión para generar un token y luego poder consultar todos los eventos disponibles y agregar nuevos. Desarrollada en Node con Express y MongoDB para la persistencia de los datos.

##API ENDPOINTS
###POST api/users/

Agregar un nuevo usuario

Estructura JSON
POST /api/users <br/>
Content-Type: application/json <br/>
<br/>
{<br/>
  "username": String,<br/>
  "password": String<br/>
}<br/>

--- 

###POST api/login/

Iniciar sesión, se genera un token

Estructura JSON
POST /api/login <br/>
Content-Type: application/json<br/>
<br/>
{<br/>
  "username": String,<br/>
  "password": String<br/>
}<br/>

---

###POST api/event/

Agregar un nuevo evento

POST /api/events<br/> 
Content-Type: application/json<br/>
Authorization: Bearer<br/>
<br/>
{<br/>
"titulo": String,<br/> 
"descripcion": String,<br/> 
"lugar": String,<br/> 
"fechas": [Date],<br/> 
"destacado": Boolean,<br/> 
"imagen": String<br/>
}
