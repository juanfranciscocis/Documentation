# Crear Nota de Crédito Perú

<procedure>
    <step>
        <p><a href="#intro">Introducción</a></p>
    </step>
    <step>
        <p><a href="#crear">Crear y enviar la Nota de Crédito</a></p>
    </step>
    <step>
        <p><a href="#aprobar">Aprobar o Rechazar Nota de Crédito</a></p>
    </step>
    <step>
        <p><a href="#sharepoint">SharePoint Base de Datos</a></p>
    </step>

</procedure>


## Introducción {id="intro"}

Esta es una guía para crear una Nota de Crédito en el sistema de Perú. La app consta de varios procesos
que se deben seguir para crear una Nota de Crédito. Estos procesos se encuentran en el siguiente orden:
1. Crear y enviar la Nota de Crédito
2. Aprobar o Rechazo de la Nota de Crédito (Existen varias aprobaciones por área)
3. Descargar Nota de Crédito en el idioma correspondiente

## Crear y enviar la Nota de Crédito {id="crear"}
[Iniciar Sesión](https://apps.powerapps.com/play/e/default-2a967794-c4d1-4bc2-8036-1a5201a5d767/a/fb550e6a-807f-4f1d-9d30-3e919b9a6a43?tenantId=2a967794-c4d1-4bc2-8036-1a5201a5d767&hint=23295a47-e9f9-4c4e-9cf4-43d1b2bdd16c&sourcetime=1697120679095)
<procedure>
    <step>
        <p>Acceso a la app: Inicie sesión en la app y navegue hasta la sección de Nueva Solicitud NC.</p>
    </step>
    <step>
        <p>Crear una nueva solicitud: En la interfaz de la app, rellene los campos necesarios para crear una nueva solicitud.</p>
        <img src="../images/NOTA_CREDITO_PERU/1.png" alt="1"/>
        <warning>
            <p>Los comentarios y motivos deben ser lo más detallados posibles </p>
        </warning>
        <warning>
            <p>Es posible selecionar entre dos tipos de solicitud: Por Servicio (varios SKU del Booking) o Por Booking completo (Monto total del booking).</p>
        </warning>
    </step>
</procedure>

### Nota de Crédito por Booking completo
En caso de hacer la solicitud por el monto total del booking, se debe ingresar el monto total del booking y asignarlo.
<procedure>
    <step>
        <p> Ingresar el monto total del booking </p>
        <img src="../images/NOTA_CREDITO_PERU/2.png" alt="2"/>
    </step>
    <step>
        <p> Asignar el monto total del booking </p>
        <img src="../images/NOTA_CREDITO_PERU/3.png" alt="3"/>
    </step>
    <step>
        <p> Enviar la solicitud dando click en Finalizar</p>
        <img src="../images/NOTA_CREDITO_PERU/4.png" alt="4"/>
    </step>
    <step>
        <p>Podremos verificar el estado de la nota de crédito en el menú "Consultar NC"</p>
        <img src="../images/NOTA_CREDITO_PERU/5.png" alt="5"/>
        <warning>
            <p>El estado de la nota de crédito puede ser: </p>
            <p>1. Pendiente </p>
            <p>2. Pre-Aprobada </p>
            <p>3. Aprobada </p>
            <p>4. Pre-Registrada </p>
            <p>5. Finalizada </p>
            <p>5. Rechazada </p>
            <p>6. Cancelada </p>
        </warning>
    </step>
    <step>
        <p>Verificar que el email automático de aprobación o rechazo haya llegado cada x tiempo</p>
    </step>
</procedure>


## Aprobar Nota de Crédito {id="aprobar"}

Para aprobar una nota de crédito el proceso se lo puede realizar desde el correo o instalando la extensión de Teams Approvals.
En este caso el proceso se lo realizará desde el app de Teams.

<procedure>
    <step>
        <p>Como aprobador ingresar a la app de Teams y buscar la extensión de Approvals</p>
        <a href="https://teams.microsoft.com/l/app/7c316234-ded0-4f95-8a83-8453d0876592?source=app-details-dialog">Descargar extensión</a>
    </step>
    <step>
        <p>Una vez instalada la extensión, ingresar a la extensión y buscar la solicitud de aprobación</p>
        <img src="../images/NOTA_CREDITO_PERU/6.png" alt="6"/>
    </step>
    <step>
        <p>Se nos despliega la ventana de la solicitud donde podremos aprobar o rechazar la solicitud</p>
        <img src="../images/NOTA_CREDITO_PERU/7.png" alt="7"/>
        <warning>
            <p>En algunos casos como aprobadores deberemos ingresar un comentario para aprobar o rechazar la solicitud, estos comentarios pueden ser
                tan genéricos como un "OK" o tan detallados como el #NC/TC en el caso de Tesorería.</p> 
        </warning>
    </step>
    <step>
        <p>Click en approve o reject </p>
        <img src="../images/NOTA_CREDITO_PERU/8.png" alt="8"/>
    </step>

</procedure>

## Descargar la Nota de Crédito {id="descargar"}
En caso de que la solicitud haya sido FINALIZADA, se debe descargar la nota de crédito en el idioma correspondiente.
<procedure>
    <step>
        <p> Ingresar a la app y buscar la solicitud FINALIZADA en Consultar NC </p>
        <img src="../images/NOTA_CREDITO_PERU/9.png" alt="9"/>
    </step>
    <step>
        <p> Click en el botón del idioma en el que se descarga la nota </p>
        <img src="../images/NOTA_CREDITO_PERU/10.png" alt="10"/>
        <warning>
            <p>Este proceso puede tardar unos minutos</p>
        </warning>
    </step>
    <step>
        <p> Ver adjuntos </p>
        <img src="../images/NOTA_CREDITO_PERU/11.png" alt="11"/>
    </step>
    <step>
        <p> Se descargará un archivo PDF con la nota de crédito </p>
        <img src="../images/NOTA_CREDITO_PERU/12.png" alt="12"/>
        <img src="../images/NOTA_CREDITO_PERU/13.png" alt="13"/>
    </step>
</procedure>

## SharePoint Base de Datos {id="sharepoint"}

Esta es una sección que es manejada únicamente por el equipo de Sistemas.

En este link podremos acceder a la base de datos de Sharepoint donde se almacenan las notas de crédito, roles y usuarios.
 [Ir al SharePoint](https://mt.sharepoint.com/app/pe-notasdecredito/Lists/App_NC_Aprobadores/AllItems.aspx)




