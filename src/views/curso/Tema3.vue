<template lang="pug">
.curso-main-container.pb-3
  BannerInterno(:subTitulo="'3. El papel del investigador en las ciencias sociales'")
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5
    
    .row.mb-4
      .col-12.col-xl-7(data-aos="fade-right")
        .bg-amarillo.p-4
          p.mb-4 A continuación, en el PDF El papel del investigador, se presenta que la investigación cualitativa y cuantitativa son enfoques fundamentales en la generación de conocimiento, cada uno con características y roles específicos que los hacen valiosos según el propósito del estudio. Lo invitamos a consultar el documento para ampliar esta información.
          a.d-flex.me-auto.bg-white.box-shadow.cursor-pointer.w-fit(data-aos="zoom-in" :href="obtenerLink('/downloads/Anexos_El papel del investigador.pdf')" target="_blank")
            img.h-100(style="width: 48px" src='@/assets/componentes/pdf-icon-square.svg', alt='Texto que describa la imagen')
            p.text-small.fs-14px.my-auto.px-2.w-fit <strong>Anexo.</strong> El papel del investigador
      .col-5.d-none.d-md-block(data-aos="fade-left")
        img(src='@/assets/curso/unidad/img-53.png', alt='Texto que describa la imagen')

    .bg-full-width.border-top-9-azul
      .px-4.px-md-5.pt-5.pb-0
        h2 Material complementario
        .row
          .col-12.col-md-6.col-lg-8
            p.d-flex.my-4
              img.me-3.mb-auto.mt-1(src='@/assets/componentes/link.svg' :style="{'max-width':'16px'}")
              a.text-small.text-primary(target="_blank", href="http://www.scielo.org.co/scielo.php?pid=S0121-32612009000100010&script=sci_arttext") Abello Llanos, R. (2009). La investigación en ciencias sociales: sugerencias prácticas sobre el proceso. Investigación y desarrollo, 17(1), 208-229
            p.d-flex.my-4
              img.me-3.mb-auto.mt-1(src='@/assets/componentes/link.svg' :style="{'max-width':'16px'}")
              a.text-small.text-primary(target="_blank", href="http://scielo.senescyt.gob.ec/scielo.php?script=sci_arttext&pid=S2550-65872024000200077&lang=es") Barahona, G., León, V., & Barzola, Y. (2024). La intervención social en personas con situaciones vulnerables. Revista de Ciencias Humanísticas y Sociales (ReHuSo), 9(2), 77-91. 
            p.d-flex.my-4
              img.me-3.mb-auto.mt-1(src='@/assets/componentes/link.svg' :style="{'max-width':'16px'}")
              a.text-small.text-primary(target="_blank", href="https://www.scielo.org.mx/scielo.php?script=sci_arttext&pid=S1405-94362023000200111&lang=es") Lione, S. V. (2023). Género, trabajo científico y reproducción social. Una aproximación conceptual para su abordaje en y desde la periferia. La ventana. Revista de estudios de género, 7(58), 111-145.
          .col-12.col-md-6.col-lg-3
            figure
              img(src='@/assets/componentes/material-complementario.svg', alt='Texto que describa la imagen')

    .bg-full-width.border-top.actividad(style="background-color: #ebf1f5; border-top: 5px solid #f5c145 !important")
      .p-4.p-md-5
        #Actividad                
          <Actividad :cuestionario="cuestionario"/>


</template>

<script>
import BannerInterno from '../../components/plantilla/BannerInterno'
export default {
  name: 'Tema3',
  components: {
    BannerInterno,
  },
  data: () => ({
    cuestionario: {
      tema: 'Metodología de Investigación - Unidad 1',
      titulo: 'Ponte a prueba',
      introduccion:
        'Demuestra lo que aprendiste en esta unidad y pon a prueba tus conocimientos.',
      barajarPreguntas: true,
      preguntas: [
        {
          id: 1,
          texto:
            'Utilizar metodologías rigurosas en investigación permite generar conocimientos valiosos que no solo describen los fenómenos, sino que también contribuyen a la resolución de problemas sociales ¿Cuál de las siguientes es una característica de la investigación cualitativa?',
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Se basa principalmente en datos estadísticos.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Busca comprender significados y experiencias subjetivas.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Utilizar solo encuestas estructuradas.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Se ejecuta únicamente en entornos controlados.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 2,
          texto:
            'El investigador desempeña un papel fundamental no solo como recopilador de datos, sino también como intérprete de estos. Al realizar una investigación social, el investigador debe:',
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Mantenerse completamente alejado de los participantes.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Ignorar los resultados que no se ajustan a sus expectativas.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Implicarse de manera ética y reflexiva en su investigación.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto: 'No considerar su propio sesgo o perspectiva.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 3,
          texto:
            'La rigurosidad asegura que la investigación esté bien fundamentada desde el diseño del estudio hasta la recolección y análisis de datos ¿Qué describe mejor el enfoque cuantitativo en la investigación?',
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'El uso de datos numéricos y análisis estadístico.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto:
                'La exploración profunda de las percepciones individuales.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'El uso exclusivo de entrevistas abiertas.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Un diseño de investigación flexible y no estructurado.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 4,
          texto:
            'La contextualización es clave en el escenario investigativo, ya que los investigadores reconocen el significado de las acciones o experiencias humanas. En el contexto de la investigación social, la "metodología" se refiere a:',
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'La forma de recopilación de datos y el cronograma de actividades.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'El manejo de software para el análisis de datos.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'El conjunto de métodos y procedimientos para llevar a cabo la investigación.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto:
                'La estimación de costos del estudio y el tipo de instrumentos a emplear.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 5,
          texto:
            'El investigador debe manejar de forma efectiva la recolección y análisis de datos tanto cuantitativos como cualitativos, utilizando métodos y técnicas distintas para cada uno. ¿Cuál es el papel del investigador en el análisis de datos cualitativos?',
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Interpretar los datos buscando patrones y significados.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Solo reportar lo que dijeron los participantes.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Centrarme en estadísticas y gráficos.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Ignorar el contexto de las respuestas.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
      ],
      mensaje_final_aprobado: '¡Excelente! Ha superado la actividad.',
      mensaje_final_reprobado:
        'Le recomendamos volver a revisar el componente formativo e intentar nuevamente la actividad didáctica.',
    },
  }),
  mounted() {
    this.$nextTick(() => {
      this.$aosRefresh()
    })
  },
}
</script>

<style lang="sass">
.material-complementario
  padding-top: 3rem
  border-top: 9px solid $color-sistema-e
</style>
