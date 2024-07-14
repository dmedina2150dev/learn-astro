# learn-astro

Caracteristicas de Astro

1. Rendimiento optimizado por defecto
2. Experiencia al desarrollador
3. SEO Friendly
4. ECMAScript moderno y Typescript
5. Extensibilidad y personalización
5. Crece acorde a la necesidad


## Código que podemos generar con Astro

1. Static Site Generation
- Se genera en just in time 
2. Server Side Rendering
- Renderizado del lado del servidor
3. Hybrid 
- Hibrido entre STG & SSR
4. Multi-Page Applications 
- Es diferente a un SPA, es una aplicación con multiples páginas en las que podemos compartir estado
5. Client-side rendering 
- Para poder utilizar una libreria o Framework de UI

## Más Herramientas
1. Server Actions
2. Astro DB
3. View Transitions
4. Pre-fetch
5. Vite - Funciona con el compilador de Vite
6. Middlewares
7. Mucho más


## Cons de Astro
1. SPA's (Single page applications) no es su enfoque, para esto mejor usar los frameworks tradicionales
2. La comunidad va creciendo, pero no es tan grande aún
3. La interactividad es un trabajo manual que depende de Vanilla Javascript/Typescript o UI Frameworks (Islas)
4. Integrar frameworks o librerias de UI, requiere tener las bases de esas tecnologias.

# Referencias a la Documentación Oficial

[Estructura de proyecto](https://docs.astro.build/es/basics/project-structure/)

[Astro preferencias](https://docs.astro.build/es/reference/cli-reference/#astro-preferences)


## NOTAS:

> Existen nombres de directorios reservados para Astro (Investigar nombres)

> Recomendado crear los archivos de Astro que serviran de componentes con CamelCase

> Existen componentes reutilizables que debemos tener la consideración anterior mencionada. 

> Existen los [Layouts](https://docs.astro.build/en/basics/layouts/)

> INTERESANTE DE ASTRO EN TYPESCRIPT
```Typescript

interface Props {
	title: string;
}

const { title } = Astro.props
```
Astro infiere las props que pasamos de esta forma.


> Guia para los [Estilos en Astro](https://docs.astro.build/en/guides/styling/)

```
<!-- No encapsulado al componente -->
<style is:global>

<!-- Astro no procesa la etiqueta y la deja tal cual como la añadimos -->
<style is:inline>

<!-- Le dice al compilador de Astro que no toque el elemento que lo deje tal cual, que lo trate como un elemento tipo texto -->
<style is:raw>
```

> View Transitions [Doc Oficial](https://docs.astro.build/en/guides/view-transitions/)

Cuando añadimos el component que lo hicimos en el head del layout, le dice al compilador de Astro que relice el pre - fetch de los de links y los enlaces de mi aplicación, para que funciones las transiciones mas rapidas.

> Como agregar Tailwind en Astro [Doc Oficial](https://docs.astro.build/en/guides/styling/#tailwind)

```
pnpm astro add tailwind
```

> [Docu getStaticPaths](https://docs.astro.build/en/reference/errors/get-static-paths-required/)