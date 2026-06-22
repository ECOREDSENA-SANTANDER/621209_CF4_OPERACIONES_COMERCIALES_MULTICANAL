<template lang="pug">
  .curso-main-container.pb-3
    BannerInterno(icono="far fa-question-circle" titulo="Actividad didáctica")
    .container.tarjeta.tarjeta--blanca.p-4.p-md-5
      // Para cuestionario usar: ActividadController(:cuestionario="cuestionario") 
      // Para parrafo usar: ActividadController(:parrafo="parrafo")
      ActividadController(:cuestionario="cuestionario")
  </template>

<script>
import ActividadController from '@ecored-sena/base-kit/plugin/components/actividad/ActividadController.vue'

export default {
  name: 'ActividadDidactica',
  components: {
    ActividadController,
  },
  data: () => ({
    cuestionario: {
      tema: 'Manejo de inventarios en el <i>Retail</i>',
      titulo: 'Cuestionario',
      introduccion:
        '<b> Objetivo:</b> verificar la comprensión de los conceptos fundamentales relacionados con la gestión logística de inventarios, la toma física y digital, el conteo de existencias, la mercancía, los productos, el <i>stock</i> y la gestión de devoluciones en el <i>retail</i>. ',
      barajarPreguntas: true,
      titulo_aprobado: '¡BUEN TRABAJO!',
      titulo_reprobado: 'VUELVA A INTENTARLO',
      preguntas: [
        {
          id: 1,
          texto:
            'En la logística comercial de un punto de venta, el inventario cumple principalmente la función de:',
          imagen: require('@/assets/actividad/imagen1.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Reemplazar los procesos de venta directa al cliente.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Eliminar la necesidad de almacenamiento y transporte.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Controlar y disponer bienes para garantizar la disponibilidad del producto.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto:
                'Registrar únicamente los productos que ya fueron vendidos.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 2,
          texto:
            'Cuando un establecimiento calcula las compras futuras para mantenerse abastecido, aplica el concepto de:',
          imagen: require('@/assets/actividad/imagen2.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Gestión de devoluciones.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Previsión de la demanda.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Avería intermitente.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Producto terminado.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 3,
          texto:
            'Un inventario continuo se diferencia de un inventario periódico porque:',
          imagen: require('@/assets/actividad/imagen3.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Se realiza solo al cierre contable anual.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Se limita a contar productos terminados.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'No requiere registrar entradas ni salidas.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Se actualiza de forma constante y permite conocer el <i>stock</i> en tiempo real.',
              esCorrecta: true,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 4,
          texto:
            'Si una empresa registra materiales que serán transformados durante el proceso productivo, clasifica ese inventario como:',
          imagen: require('@/assets/actividad/imagen4.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Materias primas.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Productos terminados.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: '<i>Stock</i> máximo.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Mercancía en devolución.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 5,
          texto:
            'En una sala de ventas con alto volumen de referencias, el uso de herramientas digitales de inventario permite:',
          imagen: require('@/assets/actividad/imagen05.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Evitar por completo la participación del personal logístico.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Sustituir las normas de manejo de mercancía.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Registrar, organizar y generar reportes de existencias para apoyar decisiones.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto: 'Eliminar la necesidad de realizar conteos físicos.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 6,
          texto:
            'El código de barras resulta útil en la gestión de productos porque:',
          imagen: require('@/assets/actividad/imagen6.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Define automáticamente el precio de venta sin control empresarial.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Automatiza la identificación del producto y reduce errores de registro.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Reemplaza los reportes de ventas semanales.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Evita cualquier proceso de devolución.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 7,
          texto: 'El dígito de verificación en un código de barras sirve para:',
          imagen: require('@/assets/actividad/imagen7.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Indicar el lugar exacto de exhibición en la góndola.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Definir si el producto es perecedero o no perecedero.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Establecer la fecha de vencimiento del producto.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Comprobar que la información del código sea correcta y segura.',
              esCorrecta: true,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 8,
          texto: 'La toma física de inventario consiste en:',
          imagen: require('@/assets/actividad/imagen8.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Verificar la existencia real, el estado y las condiciones de los bienes.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto:
                'Registrar únicamente las ventas realizadas en las últimas 24 horas.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Proyectar la demanda sin revisar las existencias.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Coordinar exclusivamente el retorno de productos al proveedor.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 9,
          texto: 'En una toma física, el acta de inicio y terminación permite:',
          imagen: require('@/assets/actividad/imagen9.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Cambiar la clasificación legal de la mercancía.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Evitar la comparación entre bienes físicos y registros contables.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Dejar registro formal del proceso, responsables, resultados y ajustes.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto: 'Eliminar la necesidad de conclusiones o recomendaciones.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 10,
          texto: 'La toma digital de inventario se caracteriza por:',
          imagen: require('@/assets/actividad/imagen10.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Depender solo de observaciones manuales en la góndola.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Utilizar sistemas automatizados para administrar movimientos de <i>stock</i>.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Realizarse sin captura ni procesamiento de información.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Aplicarse únicamente a productos deteriorados.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 11,
          texto:
            'Si el conteo se realiza al recibir mercancía de proveedores o al preparar pedidos para clientes, corresponde a:',
          imagen: require('@/assets/actividad/imagen1.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Conteo de precisión.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Inventario anual de <i>stock</i>.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Validación de <i>stock</i> agotado.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Conteo cíclico por fecha.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 12,
          texto:
            'En el procedimiento de conteo en <i>retail</i>, comparar los listados del auditor y del contador permite:',
          imagen: require('@/assets/actividad/imagen2.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Eliminar la responsabilidad del equipo de verificación.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Asignar precios nuevos a todos los productos.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Omitir el reconteo de las referencias con duda.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Validar diferencias, corregir errores y registrar información confiable.',
              esCorrecta: true,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 13,
          texto: 'Una mercancía adquiere la condición de carga cuando:',
          imagen: require('@/assets/actividad/imagen3.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Permanece exhibida sin movimiento en la góndola.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Se convierte en producto terminado para la venta.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Va a ser trasladada o enviada desde un punto de origen a un destino.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto: 'Se registra como referencia dentro del surtido.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 14,
          texto:
            'La normativa para el manejo de mercancías orienta principalmente:',
          imagen: require('@/assets/actividad/imagen4.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'La creación de campañas comerciales del punto de venta.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'La gestión segura, eficiente y legal durante la cadena logística.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'La eliminación de todos los formatos de control.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'La selección de colores y diseños de los productos.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 15,
          texto: 'Desde el enfoque comercial, un producto se entiende como:',
          imagen: require('@/assets/actividad/imagen05.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Aquello que el consumidor recibe cuando realiza una compra y le aporta beneficios.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Un elemento que nunca necesita almacenamiento.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Una mercancía que no puede intercambiarse.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Un bien que solo existe durante el proceso de devolución.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 16,
          texto: 'La rotación de productos permite:',
          imagen: require('@/assets/actividad/imagen6.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Evitar la entrada y salida de mercancía en el almacén.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Mantener productos caducados mientras exista espacio disponible.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Suspender la reposición de nuevas existencias.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Suministrar nuevas existencias y evitar pérdidas por caducidad o vencimiento.',
              esCorrecta: true,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 17,
          texto: 'Un producto agotado se presenta cuando:',
          imagen: require('@/assets/actividad/imagen7.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Cuenta con fecha de caducidad vigente.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Tiene alta rotación dentro del punto de venta.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'No está disponible para la venta en el punto o en el espacio accesible al comprador.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto:
                'Hace parte del <i>stock</i> de seguridad del establecimiento.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 18,
          texto: 'El <i>stock</i> de seguridad se mantiene para:',
          imagen: require('@/assets/actividad/imagen8.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Eliminar los conteos de inventario durante el año.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Responder ante imprevistos de demanda o retrasos de proveedores.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Almacenar solo productos sin fecha de vencimiento.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Sustituir el <i>stock</i> máximo de la empresa.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 19,
          texto: 'En la logística inversa, la devolución busca principalmente:',
          imagen: require('@/assets/actividad/imagen9.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Coordinar el retorno de productos y recuperar <i>stock</i> considerando trámites y manejo posterior.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto:
                'Aumentar la exhibición de productos averiados en góndola.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Evitar cualquier registro administrativo del producto devuelto.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Eliminar la necesidad de reetiquetado, reciclaje o disposición final.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 20,
          texto: 'Un reporte de ventas semanal es útil porque:',
          imagen: require('@/assets/actividad/imagen10.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Reemplaza el control de inventarios físicos y digitales.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Permite conocer únicamente la fecha de compra de cada cliente.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Impide revisar el comportamiento de los productos en góndola.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Ayuda a identificar situaciones que deben abordarse de manera inmediata en ventas.',
              esCorrecta: true,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
      ],
      mensaje_final_aprobado: 'Ha superado la actividad.',
      mensaje_final_reprobado:
        'Le recomendamos volver a revisar el componente formativo e intentar nuevamente la actividad didáctica.',
    },
  }),
}
</script>
