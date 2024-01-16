# PDF Butler

<procedure>
    <step>
        <p><a href="#intro">Documentación Introducción</a></p>
    </step>
    <step>
        <p><a href="#crear">Crear un DataSource</a></p>
    </step>
    <step>
        <p><a href="#config"> Configurar el Documento</a></p>
    </step>
    <step>
        <p><a href="#salesforce"> Cómo usarlo en Salesforce</a></p>
    </step>
</procedure>

## Documentación Introducción {id="intro"}

PDF Butler es una herramienta de Salesforce que permite crear documentos PDF de manera sencilla y rápida. En este caso, la documentación se encuentra en 
su página oficial, la cual permite a los desarrolladores y usuarios acceder a la documentación de manera sencilla y rápida.
<a href="https://www.pdfbutler.com/academy.html">Ir a la Documentación</a>

En este documento se detalla de manera sencilla y rápida el uso de PDF Butler en el ambiente de Salesforce.


## Uso PDF Butler {id="crear"}

Es necesario saber que PDF Butler es una herramienta basada en SQL, por lo que es necesario tener conocimientos básicos de SQL para poder utilizarla. 

<procedure>
    <step>
        <p>Abrir el completo en SalesForce</p>
        <img src="../images/PDF_BUTLER/1.png" alt="1"/>
        <p>La página principal muestra videos documentales de la app</p>
    </step>
    <step>
        <p>Para crear un nuevo documento debemos ir a la sección de "Data Sources" -> New</p>
        <img src="../images/PDF_BUTLER/2.png" alt="2"/>
    </step>
    <step>
        <p>Seleccionamos SOQL</p>
        <img src="../images/PDF_BUTLER/3.png" alt="3"/>
    </step>
    <step>
        <p>Rellenamos los datos como Data Source Name, Description ... </p>
        <img src="../images/PDF_BUTLER/4.png" alt="4"/>
        <warning>
            <p>Normalmente utilizamos como Type: List of sObjects</p>
        </warning>
        <warning>
            <p>El Apartado de Data Child Source Settings es para cuando queremos crear un documento que tenga un subdocumento, aquí van entonces las relaciones
            entre los objetos de tipo Data Source</p>
        </warning>
    </step>
    <step>
        <p>En el apartado de SOQL Query debemos ingresar la consulta SQL que queremos realizar</p>
        <img src="../images/PDF_BUTLER/5.png" alt="5"/>
    </step>
    <step>
        <p>Guardamos el Data Source</p>
    </step>
    <step>
        <p>Llegados a este punto, deberíamos ser capaces de comenzar a generar el PDF o archivo Word, pero normalmente
        requerimos de más Data Sources para crear relaciones, para este ejemplo se crea un Data Source extra que se muestra aquí</p>
        <img src="../images/PDF_BUTLER/6.png" alt="6"/>
        <warning>
            <p>Como se puede ver en la imagen el DataSource hace referencia a otro DataSource(Opportunity), agrupando por
                Opportunity.Id y filtrando por el Id de la Opportunity que se está visualizando</p>
        </warning>
    </step>
</procedure>

## Configurar el Documento {id="config"}

Aquí es donde se unen las consultas SQL con el documento que se quiere generar, para este ejemplo se va a generar un documento
en formato Word

<procedure>
    <step>
        <p>Vamos a la sección Doc Configs -> New (Por recomendación crear como Main Word Document)</p>
        <img src="../images/PDF_BUTLER/7.png" alt="7"/>
    </step>
    <step>
        <p>Rellenamos el nombre de documento, título, descripción y siempre generamos el tipo de Delivery Option como Attachment</p>
        <img src="../images/PDF_BUTLER/8.png" alt="8"/>
    </step>
    <step>
        <p>Click en Save y abrimos el editor</p>
        <img src="../images/PDF_BUTLER/9.png" alt="9"/>
    </step>
    <step>
        <p>Comenzamos a elegir los Data Sources que queremos utilizar</p>
        <img src="../images/PDF_BUTLER/10.png" alt="10"/>
    </step>
    <step>
        <p>Al elegir un Data Source se nos despliega un menú con los campos que podemos utilizar</p>
        <img src="../images/PDF_BUTLER/11.png" alt="11"/>
        <warning>
            <p>Si las consultas fueron correctamente realizadas, los campos deberían aparecer en el menú</p>
        </warning>
    </step>
    <step>
        <p>Click en OK</p>
    </step>
    <step>
        <p> De igual forma si las relaciones entre Data Sources fueron correctamente realizadas, cuando presionamos sobre New Child </p>
        <img src="../images/PDF_BUTLER/12.png" alt="12"/>
        <img src="../images/PDF_BUTLER/13.png" alt="13"/>
    </step>
    <step>
        <p>Ahora podemos configurar el documento como queramos, agregando campos, imágenes, tablas, etc.</p>
        <img src="../images/PDF_BUTLER/14.png" alt="14"/>
        <warning>
            <p>Lo correcto es partir de un documento word con el formato preparado por ejemplo:</p>
            <img src="../images/PDF_BUTLER/15.png" alt="15"/>
        </warning>
    </step>
    <step>
        <p>Ahora vamos a ver como se configura una tabla, la tabla que vemos arriba de Word</p>
        <img src="../images/PDF_BUTLER/16.png" alt="16"/>
        <p>Podemos ver que se ingresa un nombre, el tipo que es un TABLE_ROW, el DataSource y el MergeField que es el campo que queremos mostrar OPP en el Word</p>
    </step>
    <step>
        <p>Vamos a crear tantos ConfigTypes como necesitemos, en este caso la siguiente row se ve así</p>
        <img src="../images/PDF_BUTLER/17.png" alt="17"/>
        <p>Podemos ver que como estamos creando la tabla el nombre es el lo que antes era el MergeField, el tipo es SINGLE y el DataSource es configurable como queramos, el DataSourceField en este caso es el ID de la Opportunity y finalmente el MergeField también es OPP</p>
        <warning>
            <p>Así es como nos va quedando entonces el árbol</p>
            <img src="../images/PDF_BUTLER/18.png" alt="18"/>
        </warning>
        <warning>
            <p>Es importante que el MergeField del Table Row no se llama igual al primer campo de la tabla da problemas</p>
        </warning>
    </step>
    <step>
        <p>Debemos ir configurando el documento como queramos, antes de continuar </p>
        <warning>
            <p>Para el ejemplo que estamos haciendo los campos quedan así</p>
            <img src="../images/PDF_BUTLER/20.png" alt="20"/>
            <p>Para el ejemplo que estamos haciendo el PDF queda de esta manera</p>
            <img src="../images/PDF_BUTLER/19.png" alt="19"/>
        </warning>
    </step>
    <step>
        <p>Una vez que hemos terminado de configurar el documento debemos ir a la sección de "Doc Config Documents" y subir el Word que hemos configurado</p>
        <img src="../images/PDF_BUTLER/21.png" alt="21"/>
    </step>
    <step>
        <p>Ahora damos en Save to Server donde nos vamos a dar cuenta si el proceso es o no exitoso</p>
        <img src="../images/PDF_BUTLER/22.png" alt="22"/>
        <warning>
            <p>Si el proceso es exitoso, vemos un indicador verde</p>
        </warning>
    </step>
    <step>
        <p>Ahora podemos descargar el documento, Test Conversion </p>
        <img src="../images/PDF_BUTLER/23.png" alt="23"/>
    </step>
    <step>
        <p>Descargamos por ejemplo en formato DOCX</p>
        <img src="../images/PDF_BUTLER/24.png" alt="24"/>
    </step>
</procedure>

## Cómo usarlo en Salesforce {id="salesforce"}

El ID que devuelve el objeto en PDF Butler es clave para poder utilizarlo en Salesforce

<procedure>
    <step>
        <p>Podemos obtener el ID del link del objeto</p>
        <img src="../images/PDF_BUTLER/25.png" alt="25"/>
    </step>
    <step>
        <p>Regresamos a Metropolitan Touring en la sección de Apps</p>
        <img src="../images/PDF_BUTLER/26.png" alt="26"/>
    </step>
    <step>
        <p>Vamos a un objeto donde queramos agregar el reporte, en este caso una oportunidad, en la parte inferior vemos que se encuentra el plugin de PDF Butler</p>
        <img src="../images/PDF_BUTLER/27.png" alt="27"/>
    </step>
    <step>
        <p>Para agregar una nueva sección debemos dar click en el botón de configuración -> Edit Page</p>
        <img src="../images/PDF_BUTLER/28.png" alt="28"/>
        <img src="../images/PDF_BUTLER/29.png" alt="29"/>
    </step>
    <step>
        <p>Arrastramos el componente de PDF Butler a la sección que queramos</p>
        <img src="../images/PDF_BUTLER/30.png" alt="30"/>
    </step>
    <step>
        <p>Configuramos el componente, ingresando el ID que obtuvimos anteriormente</p>
        <img src="../images/PDF_BUTLER/31.png" alt="31"/>
        <warning>
            <p>Podemos configurar filtros, emails automáticos, etc.</p>
        </warning>
    </step>
    <step>
        <p>Guardamos y activamos la página</p>
    </step>
    <step>
        <p>Probamos viendo la oportunidad y la nueva sección que hemos creado</p>
        <img src="../images/PDF_BUTLER/32.png" alt="32"/>
    </step>
    <step>
        <p>Podemos ver que el documento se ha generado correctamente</p>
        <warning>
            <p>Si el documento no se genera correctamente, debemos revisar los Data Sources y el documento, además la consola</p>
        </warning>
    </step>
</procedure>
