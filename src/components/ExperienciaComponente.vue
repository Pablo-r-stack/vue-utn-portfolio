<script setup>
import icono1 from '/src/assets/ventas.svg'
import icono2 from '/src/assets/ecomerce.svg'
import icono3 from '/src/assets/configuracion.svg'
import icono4 from '/src/assets/uiux.svg'
import icono5 from '/src/assets/watch.svg'

import { ref } from 'vue'
const experiencias = ref([
  {
    id: 1,
    puesto: 'Desarrollador Full Stack',
    empresa: 'Fuerte Digital',
    periodo: '09/2025 – 11/2025',
    src: icono1,
    logros: [
      'Lideré un equipo de 4 desarrolladores en la creación de una plataforma web de gestión para un gimnasio de un cliente particular, reduciendo en un 70% los tiempos de gestión de alumnos, inscripciones y control de pagos.',
      'Desarrollé la interfaz de usuario para la plataforma, utilizando React, Shadcn y Tailwind CSS, mejorando la usabilidad y la experiencia del usuario en la gestión de sus datos.',
      'Implementé seguridad y guards en la aplicación frontend para proteger los datos de los usuarios y prevenir accesos no autorizados.',
      'Colaboré en el desarrollo backend utilizando Nestjs, TypeORM y MySQL, implementando un sistema programado de generación de cuotas y registro de comprobantes de pago.',
      'Desplegué y configuré en producción la aplicación en un servidor basado en Ubuntu, asegurando la disponibilidad y el rendimiento de la plataforma.',
    ],
  },
  {
    id: 2,
    puesto: 'Desarrollador Frontend',
    empresa: 'No-Country (Core Squad Dev)',
    periodo: '07/2025 – 10/2025',
    src: icono2,
    logros: [
      'Formé parte del equipo inicial de desarrollo frontend para la nueva plataforma de No-Country usando Next.js, Typescript, Shadcn y Tailwind CSS.',
      'Desarrollo de aplicación web multiplataforma, responsiva y multi-idioma utilizando NextIntl con soporte en inglés, portugués y español.',
      'Lanzamiento en producción de la plataforma No-Country para validación de talentos y simulación laboral en el ambiente IT.',
    ],
  },
  {
    id: 3,
    puesto: 'Desarrollador Frontend',
    empresa: 'Foo Talent Group',
    periodo: '04/2025 – 06/2025 | Remoto',
    src: icono3,
    logros: [
      'Desarrollo de flujos clave: login, usuarios, propiedades, contratos y pagos.',
      'Coordinación técnica del equipo frontend: stack, estructuras, convenciones y Git Flow.',
      'Participación en la definición de producto, documentación funcional y trabajo ágil con equipo interdisciplinario.',
      'Lanzamiento exitoso de Rentary, aplicación web de gestión inmobiliaria.',
    ],
  },
  {
    id: 4,
    puesto: 'Desarrollador Full Stack',
    empresa: 'No-Country',
    periodo: '07/2024 – 03/2025',
    src: icono4,
    logros: [
      'Diseño y desarrollo de aplicaciones web responsivas usando tecnologías como React, Next.js, Tailwind CSS, Shadcn, Typescript, Java y bases de datos relacionales.',
      'Desarrollo de rutas, validación de formularios y consumo de REST API, con manejo dinámico de vistas y componentes.',
      'Entrega y presentación de proyectos: “Pasos Firmes” (banco ortopédico online), “WorkWise” (gestión de recursos humanos) y participación en el hackatón “KlowHub” (plataforma de aprendizaje low-code).',
      'Lideré cinco equipos de desarrollo, guiando planificación, ejecución y entrega de sus MVPs.',
    ],
  },
  {
    id: 5,
    puesto: 'Desarrollador Full Stack',
    empresa: 'Codo a Codo',
    periodo: '03/2024 – 07/2024',
    src: icono5,
    logros: [
      'Líder técnico: gestión del repositorio del proyecto e integración de código.',
      'Diseño y maquetado UI inicial utilizando Figma.',
      'Desarrollo de una aplicación web responsiva basada en HTML5 + Vanilla JS, NodeJs y Express con MySql.',
      'Módulo de validación de formularios, conexión al servidor mediante API Rest, manejo de cookies y session storage para credenciales.',
      'Desarrollé el backend de la aplicación basado en NodeJs y Express, implementando rutas, controladores y servicios para la gestión de la plataforma en general.',
      'Presentación del proyecto “Sonica” como tramo final de Programación Full Stack con Node.js (Codo a Codo).',
    ],
  },
  {
    id: 6,
    puesto: 'Desarrollador Frontend',
    empresa: 'No-Country',
    periodo: '02/2024 – 03/2024',
    src: icono1,
    logros: [
      'Diseño y maquetado UI inicial utilizando Figma.',
      'Manejo del repositorio del proyecto e integración de código.',
      'Desarrollo frontend de una aplicación web responsiva utilizando React + JS orientada a clientes.',
      'Lanzamiento de “Your Online Wallet”, billetera virtual para simplificar pagos y transacciones.',
    ],
  },
  {
    id: 7,
    puesto: 'Desarrollador Full Stack',
    empresa: 'Egg Live',
    periodo: '11/2023 – 12/2023',
    src: icono2,
    logros: [
      'Desarrollo de una aplicación web SSR basada en Java + Spring y motor de plantillas Thymeleaf.',
      'Desarrollo web responsivo utilizando HTML + CSS, creación de rutas y comportamiento basado en roles de usuario.',
      'Entrega del proyecto “Quincho Club”, sitio web orientado al alquiler de espacios para eventos privados.',
    ],
  },
])
</script>

<template>
  <div class="card">
    <ul class="listado">
      <li class="item" v-for="experencia in experiencias" :key="experencia.id">
        <img class="imagen-svg" :src="experencia.src" width="45rem" :alt="experencia.puesto" />
        <div class="contenido">
          <h3 class="titulo">{{ experencia.puesto.toLocaleUpperCase() }}</h3>
          <p class="fecha">{{ experencia.empresa }} · {{ experencia.periodo }}</p>
          <ul class="logros">
            <li v-for="(logro, i) in experencia.logros" :key="i">{{ logro }}</li>
          </ul>
        </div>
      </li>

      <!-- <li class="item"><img class="imagen-svg" src="/src/assets/ventas.svg" width="45rem" alt="">
                <p>Lideré un equipo de 5 desarrolladores en la creación de una plataforma de comercio electrónico que incrementó las ventas en un 35% durante el primer año.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/ecomerce.svg" width="45rem" alt="">
                <p>Diseñé y desarrollé aplicaciones web utilizando Node.js, React y MongoDB, logrando reducir el tiempo de carga de las páginas en un 50%.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/configuracion.svg" width="45rem" alt="">
                <p>Implementé soluciones de autenticación y autorización, mejorando la seguridad del sitio web y reduciendo los intentos de acceso no autorizado en un 20%.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/uiux.svg" width="45rem" alt="">
                <p>Colaboré con diseñadores de UX/UI para crear interfaces de usuario atractivas y fáciles de usar, aumentando la satisfacción del cliente en un 15%.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/watch.svg" width="45rem" alt="">
                <p>Automaticé procesos de despliegue continuo utilizando Jenkins y Docker, reduciendo los tiempos de despliegue en un 40%.</p>
            </li> -->
    </ul>
  </div>
</template>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  padding: 2rem;
  background-color: rgb(28, 41, 52);
  border-radius: 15px;
}

.titulo {
  font-size: 1.5rem;
  color: coral;
}

.fecha {
  font-size: 1rem;
  color: burlywood;
  margin-bottom: 1rem;
}

.listado {
  display: flex;
  flex-direction: column;
}

.item {
  align-items: flex-start;
  display: flex;
  padding: 1rem;
  gap: 1.5rem;
}

.contenido {
  display: flex;
  flex-direction: column;
}

.logros {
  margin: 0.5rem 0 0;
  padding-left: 1.2rem;
}

.logros li {
  margin-bottom: 0.5rem;
}
</style>
