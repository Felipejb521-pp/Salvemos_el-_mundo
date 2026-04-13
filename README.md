Este proyecto es una versión optimizada de la página de aterrizaje de GreenTech. El objetivo principal de la refactorización fue eliminar la "grasa digital".
Se han eliminado las dependencias externas que ralentizaban la carga:

          Bootstrap (CSS): Se eliminó el enlace al framework completo. En su lugar, se creó CSS Nativo para el diseño del Hero, el botón y el footer.
        
          FontAwesome: Se sustituyó la librería de iconos por un carácter Unicode (&#127811;). Esto ahorra la descarga de una fuente entera para mostrar un solo icono.
        
          Bootstrap (JS): Se eliminó el script de Bootstrap ya que las funciones interactivas no eran necesarias para esta estructura.

La imagen de fondo de Unsplash se ha configurado con parámetros directamente en la URL:

          q=75: Reduce la calidad al 75%.
        
          w=1920: Limita el ancho máximo a 1920px para evitar descargar resoluciones innecesarias.
          
Como ya no dependemos de Bootstrap, creamos reglas específicas en la etiqueta <style> para replicar el comportamiento visual:

          h1: Sustituye a display-1 y fw-bold.
          
          .texto-subtitulo: Sustituye a lead, fs-3 y mt-3.
          
          .btn-eco-redundante: Estilizado manualmente con sombras y bordes redondeados.
          
          .footer-estilo: Define el fondo oscuro y el texto centrado que antes dependía de bg-dark y text-center.
