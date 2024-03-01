# ***Introducción a React***
1. ### ***¿Qué es React.js?*** 
Es una biblioteca de JavaScript que se utiliza para construir interfaces de usuario. React también es una aplicación de una sola página. Por tanto, en lugar de enviar una petición al servidor cada vez que hay que renderizar una nueva página, el contenido de la página se carga directamente desde los componentes de React. 

2. ### ***Las diferencias entre React.js versión 18.***
- **Routing:**  es la biblioteca de enrutamiento más popular para React.js. Proporciona una forma declarativa de definir las rutas de la aplicación y renderizar componentes correspondientes a esas rutas.
  **Ejemplo:**
```javascript
import { BrowserRouter as Router, Route, Switch } from 'react-router-dom';
import PaginaInicio from './PaginaInicio';
import PaginaPerfil from './PaginaPerfil';
import PaginaNotFound from './PaginaNotFound';
function App() {
  return (
    <Router>
      <Switch>
        <Route exact path="/" component={PaginaInicio} />
        <Route path="/perfil" component={PaginaPerfil} />
        <Route component={PaginaNotFound} />
      </Switch>
    </Router>
  );
}
export default App;
```
- **Rendering:**  es el proceso de convertir la estructura de componentes React en elementos de interfaz de usuario que se muestran en el navegador.
**Ejemplo:**
```javascript
// Importa la biblioteca React y ReactDOM
import React from 'react';
import ReactDOM from 'react-dom';

// Define un componente funcional en React
const MiComponente = () => {
  return React.createElement('h1', null, 'Hola Mundo!');
};

// Renderiza el componente en el DOM
ReactDOM.render(
  React.createElement(MiComponente),
  document.getElementById('root')
);
```
- **Data Fetching:** implica recuperar datos de una fuente externa, como una API web, una base de datos o un servidor.
- **Styling:** se refiere al proceso de aplicar estilos visuales a los componentes de la interfaz de usuario. Esto incluye propiedades como colores, tamaños, fuentes y márgenes para determinar el aspecto y la presentación de los elementos en la pantalla.
- **Optimizations:**  buscan mejorar la experiencia del usuario al hacer que las aplicaciones sean más rápidas, eficientes y agradables de usar, mediante la implementación de técnicas y mejores prácticas para optimizar el rendimiento y la calidad del código.
- **Typescript:** es un superconjunto tipado de JavaScript que agrega tipado estático opcional a tus programas, lo que permite detectar errores en tiempo de compilación y proporciona un mejor soporte para herramientas de desarrollo.

3. ### ***Define los siguientes conceptos detrás de React:***
I. **Components:** son bloques de construcción reutilizables para interfaces de usuario, permiten una organización modular del código y facilitan la reutilización y el mantenimiento.

II. **JSX:**(JavaScript XML), es una extensión de sintaxis para JavaScript que permite escribir código HTML dentro de JavaScript, se utiliza para describir la interfaz de usuario de la aplicación. 

III. **props:**  son objetos que pasan datos de un componente padre a un componente hijo en React. Son la principal forma de comunicación entre componentes en una aplicación React. 

IV. **state:** es un objeto que contiene datos dinámicos y controla el comportamiento de un componente en React.

4. ### ***Patrón de diseño estructural Composite, en qué consiste y cuál es su relación con React?***

<img src="https://github.com/LuisalyCompres/react_intro/blob/main/composite.png?raw=true" alt="composite" width="400">

**El patrón de diseño estructural Composite:** se utiliza para componer objetos en estructuras de árbol para representar jerarquías de parte-todo. 

**¿En qué consiste?** permite que los clientes interactúen con estructuras complejas de objetos de la misma manera que interactúan con objetos individuales. 

**La relación entre el patrón Composite y React** radica en cómo React implementa la composición de componentes para construir interfaces de usuario. En React, los componentes se pueden componer de manera jerárquica para formar la estructura de la interfaz de usuario de una aplicación. Esta composición es fundamentalmente similar al patrón Composite, donde los objetos individuales y compuestos se manejan de manera uniforme.

5. ### ***Patrón de diseño estructural State, en qué consiste y cuál es su relación con React?***
<img src="https://github.com/LuisalyCompres/react_intro/blob/main/state.png?raw=true" alt="state" width="400">

**El patrón de diseño estructural State:** se utiliza para permitir que un objeto altere su comportamiento cuando su estado interno cambia. En este patrón, el objeto delega el cambio de su comportamiento a un objeto que representa su estado actual. 


**¿En qué consiste?**  en encapsular el estado de un objeto en un objeto separado, y delegar las responsabilidades relacionadas con el estado a ese objeto. Esto permite que el objeto cambie su comportamiento cuando su estado interno cambia, sin necesidad de cambiar su clase.

**La relación entre el patrón State y React** es directa, ya que React proporciona un mecanismo fácil de usar para manejar el estado de los componentes. Al utilizar el estado en React, los desarrolladores pueden crear interfaces de usuario dinámicas y receptivas que respondan a las interacciones del usuario y a los cambios en los datos de la aplicación.
