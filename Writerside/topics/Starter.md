# Crear Pruebas en AzureDevOps Metropolitan Touring QA

## Índice de Contenidos
<procedure>
    <step>
        <p><a href="#devops-intro">DevOps Introducción</a></p>
    </step>
    <step>
        <p><a href="#quedevops">Qué son los tests en Azure DevOps</a></p>
    </step>
    <step>
        <p><a href="#crear">Crear un Test en Azure DevOps</a></p>
    </step>
    <step>
        <p><a href="#masivos">Crear Tests masivos en Azure DevOps</a></p>
    </step>
</procedure>



## DevOps Introducción {id="devops-intro"}
Azure DevOps es un conjunto de servicios que permite a los equipos de desarrollo y operaciones compartir código, 
realizar un seguimiento del trabajo y enviar software; todo en un solo lugar. Azure DevOps incluye repositorios de Git 
privados, un sistema de compilación CI/CD, tableros Kanban, seguimiento de problemas y mucho más.

En Metropilitan Touring QA, utilizamos Azure DevOps para crear y ejecutar pruebas automatizadas, además revisar los
resultados de las pruebas y generar reportes de los mismos.

Por otro lado QA utiliza Azure DevOps para revisar estados de los bugs, crear bugs, asignar bugs, etc.

Finalmente QA es también responsable de crear historias de usuario y tareas en Azure DevOps cuando se levantan procesos.

<img src="../images/devops.png" alt="DevOps" width="500" border-effect="line"/>



## Qué son los tests en Azure DevOps {id="quedevops"}
Los tests en Azure DevOps son un conjunto de pasos que se ejecutan en un ambiente de Azure DevOps, los cuales pueden
ser ejecutados de forma manual o automática.

Hoy en día en Metropolitan Touring QA, se utilizan los tests de Azure DevOps para ejecutar pruebas manuales, que son
ejecutadas por los testers de QA. Estos tests validan que los procesos, apps y/o funcionalidades de los sistemas de
Metropolitan Touring funcionen correctamente. Y todos los tests deben encontrarse en estado "Passed" para que una funcionalidad
pueda ser liberada a producción.

En caso de que el test falle, el tester de QA debe crear un bug en Azure DevOps, y asignarlo al equipo de desarrollo
para que lo resuelva. El equipo de desarrollo es quien debe cambiar el estado del bug a "Resolved for QA" y asignarlo al tester de QA para que lo valide.
Una vez que el bug es resuelto, el tester de QA debe ejecutar nuevamente TODOS los test y verificar que el bug haya sido resuelto.

**Nota: Es importante identificar el siguiente logo, ya que se utiliza para identificar los tests en Azure DevOps. Más adelante
se muestra la interfaz de Azure DevOps y se explica cómo crear un test paso a paso.**

## Crear un Test en Azure DevOps {id="crear"}

<tabs>
    <tab title="Paso 1">
        <procedure>
        <step>
        </step>
        </procedure>
    </tab>
    <tab title="Paso 2">
        <procedure>
        <step>
        </step>
        </procedure>
    </tab>
</tabs>

## Crear Tests masivos en Azure DevOps {id="masivos"}

<tabs>
    <tab title="Paso 1">
        <procedure>
        <step>
        </step>
        </procedure>
    </tab>
    <tab title="Paso 2">
        <procedure>
        <step>
        </step>
        </procedure>
    </tab>
</tabs>

[Descargar Template](https://www.jetbrains.com/help/writerside/collapsible-blocks.html)





