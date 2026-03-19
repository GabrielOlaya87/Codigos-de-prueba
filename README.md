# Códigos-de-prueba
Códigos de prueba.

#### css extra
```css
/* Ocultar checkbox */
#menu-toggle {
  display: none;
}

/* Imagen hamburguesa */
.menu-icon img {
  width: 30px;
  cursor: pointer;
}

/* Menú lateral oculto */
.menu {
  position: fixed;
  top: 0;
  left: -250px; /* escondido fuera de la pantalla */
  width: 250px;
  height: 100%;
  background: #444;
  list-style: none;
  padding: 20px;
  display: flex;
  flex-direction: column;
  gap: 15px;
  transition: left 0.3s ease; /* animación suave */
}

/* Mostrar menú cuando el checkbox está activo */
#menu-toggle:checked ~ .menu {
  left: 0; /* aparece desde la izquierda */
}

.menu li a {
  color: white;
  text-decoration: none;
}
```
