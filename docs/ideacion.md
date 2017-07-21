# Ideación: componentes + historias de usuario #

### a. Desarrollo front-end y Diseño (UI, UX, etc.) ###

### Componentes indispensables (*must*) ☝🏼 ###
**App móvil (usuario):**
- El usuario encontrará un demo/onboarding screen al abrir la aplicación si no ha iniciado sesión y bajo el apartado de “Ayuda/sobre esta aplicación” una vez iniciada la sesión.
- El usuario podrá consultar, sin necesidad de iniciar sesión,  un listado de iniciativas abiertas, con su nombre corto, fotografía, descripción, redes sociales, conteo de firmas,  liga al contenido completo y botones para firmar a título personal o sumarse como brigadista. 
- El usuario podrá filtrar el listado de iniciativas por tipo de iniciativa, por estado o por palabra clave en la barra de búsqueda. 
- Antes de dar su primer apoyo, el usuario deberá registrarse con su correo electrónico, redes sociales (facebook)  y los datos de su credencial de elector (nombre completo, clave de elector, firma, sección, código postal*) y confirmar su cuenta con un código de verificación vía SMS o email*  justo antes de firmar.
- Si la iniciativa requiere de copia de credencial de elector para validar su apoyo, se le presentará al usuario una pantalla adicional para capturar con su cámara el frente y reverso de su credencial y enviarla, especificando el requisito en la ley que lo pide.
- El usuario debe poder ser notificado si hubo un error de captura en los campos a llenar a la hora de firmar. 
- El usuario debe poder ser notificado si la clave de elector que ingresó no es válida, no está vigente o si no aplica para apoyar la iniciativa seleccionada.
- El usuario podrá hacer, repetir y confirmar una firma autógrafa digital sólo por medio de la aplicación móvil, ya sea:
   - cada que apoye una iniciativa con una leyenda que haga explícito qué está apoyando. 
   - haciendo su firma una sola vez y  cargándola a su cuenta para futuros apoyos.
- El usuario debe recibir un mensaje de confirmación que indique que su apoyo fue enviado satisfactoriamente, junto con el conteo de la iniciativa hasta el momento, días restantes, botones para compartir en redes sociales, botón para seguir apoyando esta iniciativa como brigadista y botón para seguir consultando otras iniciativas a apoyar . 
- El usuario puede elegir apoyar una iniciativa  como  firmante, dando su firma digital a título personal,  o como brigadista, donde podrá recolectar firmas digitales de otras personas.
- El usuario en modo brigadista podrá registrar los datos de una firma física y, cuando sea necesario, la fotografía de la credencial de elector, para agregarlos al conteo global.
- Al ingresar en modo brigadista, el usuario será notificado que sus datos de contacto se compartirán al promotor. 
- Una vez realizado el registro y  su primera firma, el usuario tendrá guardados en su cuenta  los datos de su credencial de elector para futuros apoyos. 
- El usuario debe poder consultar un listado de las iniciativas que ha apoyado con su firma o como brigadista.
- Una vez registrado, el usuario podrá filtrar las iniciativas que los datos de su credencial de elector le permiten firmar. 

**Aplicación web (promotor):**
- Cualquier promotor debe poder dar de alta su iniciativa en un formulario web de acuerdo a los atributos propios de cada tipo de iniciativa.
- Cada promotor debe adjuntar un comprobante sobre la solicitud formal de su iniciativa ante los autoridades electorales para poder ser dada de alta en la plataforma.
- El promotor puede elegir si habilitar un modo abierto para brigadistas o no.
- El promotor deberá proveer en el formulario:
  1. Nombre corto 
  2. Nombre completo de la iniciativa
  3. Tipo de iniciativa
  4. Iniciativa ciudadana de ley
  5. Consulta popular
  6. Candidatura independiente
  7. Local o federal
  8. Estado
  9. Distrito, municipio o estado a contender* (en caso de CIs)
  10. Descripción
  11. Contenido completo
  12. Fotografía de portada
  13. Redes sociales
  14. Comprobante de solicitud de iniciativa ante autoridades electorales.
  15. Confirmar haber leído y cumplir tanto con el código de conducta como con lo términos de privacidad y responsabilidades legales.
- El promotor será notificado por la administración si su propuesta de consulta cumple con los criterios técnicos mínimos y el código de conducta. En caso de ser rechazada, se justificará la decisión y se le dará retroalimentación por parte de la administración. 
- El promotor podrá revisar un conteo global a tiempo real sobre el número de firmas recolectadas, con algunas otras métricas como actividad de brigadistas, distribución territorial, días restantes, etc.
- El promotor podrá consultar el número de brigadistas registrados y acceder a los datos de contacto que dieron. 
- El promotor debe poder descargar en cualquier momento la totalidad de las firmas que haya recaudado en los formatos que exige el INE para cada tipo de iniciativa. 


### Componentes oportunos (*nice to have*) 👍🏼 ###
**App móvil (usuario):**
- El usuario podrá filtrar la lista de iniciativas de acuerdo a las  que corresponden a su zona electoral y las que legalmente puede  apoyar. 
- El usuario puede obtener un código o llave para apoyos subsecuentes.
- El usuario puede elegir registrarse con correo electrónico o redes sociales.
- El usuario debe poder ser notificado (push-up) si se registró una firma a su nombre.
- El usuario debe poder compartir directamente el perfil para acceder a una iniciativa con un identificador de la misma  (liga/códigoQR/código numérico/alias).
- El usuario debe poder conocer iniciativas que correspondan a su distrito local empatando datos de su sección electoral, la redistritación federal y su correspondencia con distritos locales.
- El usuario debe poder dar seguimiento a los avances de las iniciativas que ha apoyado.
- El usuario puede generar un perfil personalizado sobre las iniciativas que ha apoyado, con categorías visibles.
- El usuario en modo brigadista puede activar un punto de recolección temporal (hot spot) en un mapa.

**Aplicación web (promotor)**
- El promotor debe poder compartir directamente el perfil de una iniciativa.
- El promotor puede difundir el perfil de su iniciativa con una identificador propio (liga/códigoQR/código numérico/alias).
- El promotor puede capturar el conteo de firmas físicas e integrarlas a la métrica general. 
- El promotor debe poder hacer cortes en cualquier momento sobre el número de firmas digitales y físicas.  
- Cada promotor puede recibir donaciones para su iniciativa, de las cuales la administración recibirá una comisión para su sostenibilidad.
- El promotor puede consultar una guía sobre los atributos y procesos necesarios de cada categoría de iniciativa. 
- El promotor puede entregar digitalmente sus firmas de apoyo.

____
## b. Desarrollo back-end y arquitectura de sistemas ##

### Componentes indispensables (*must*) ☝🏼 ###
- El sistema podrá comprobar la existencia y vigencia de cada firma con la clave de elector (API scrappeada o key API oficial INE). 
- El sistema habilitará una verificación en dos pasos por SMS o correo electrónico* para confirmar el registro de un usuario al hacer su primera firma. 
- El sistema deberá generar una cuenta por usuario después de registrar su primera firma con sus datos de contacto y de su credencial de elector.
  - Nombre
  - Apellidos
  - Correo electrónico
  - Clave de elector
  - Sección electoral
  - Estado
  - Celular* (para la verificación SMS)
- El sistema subirá al listado las iniciativas aprobadas por la administración, sobre las cuales empezará a recibir datos de firmantes a los que sólo puede acceder el promotor.
- El sistema debe poder recibir los datos asociados a cada firma digital (clave de elector, nombre completo y firma autógrafa) y ordenarlos para exportarse en el formato oficial que exige la autoridad electoral.

_______
## c. Seguridad y privacidad ##

### Componentes indispensables (*must*) ☝🏼 ###
- El sistema debe facilitar un sistema de recolección de firmas razonablemente seguro y que consiga mayores capas de seguridad que las firmas en papel. 
- El sistema debe impedir que se dupliquen firmantes por iniciativa.
- El sistema  debe poder validar internamente las firmas para defender su autenticidad confirmando la existencia o vigencia de la clave de elector.
- El usuario debe confirmar su registro con una verificación de dos pasos vía SMS.  
- El promotor es el único que puede acceder al contenido de los datos recabados de firmantes y es el único responsable legal sobre su uso.
- El sistema debe garantizar la encripción de los datos, incluida la firma digital de cada usuario.
- El sistema será sometido a una auditoría abierta antes de ser utilizado.

### Componentes oportunos (*nice to have*) 👍🏼 ###
- El sistema debe poder reconocer cuando las firmas provengan de un ser humano. 
- El usuario puede validar internamente todos los apoyos que dé en la plataforma con un código o llave única. 

_____
## d. Investigación (legal, jurídica, normativa, etc.) ##

### Componentes indispensables (*must*) ☝🏼 ###
- La administración debe conformarse por un consejo de organizaciones bajo una A.C que gestione el uso de la herramienta. 
- La administración debe poder recibir solicitudes categorizadas por tipo de iniciativa y aprobarlas si es que cumplen con requisitos jurídicos, técnicos y el código de ética definido para la plataforma.
- La administración podrá rechazar y retroalimentar una iniciativa de acuerdo a criterios jurídicos, técnicos y un código de ética mínimos.
- El usuario puede apoyar iniciativas con firmas digitales autógrafas que puedan ser presentadas en el formato que especifica la ley para ser válidas junto con los datos que requiere cada figura (nombre completo, clave de elector y fotografías de credencial de elector).
- El usuario debe llenar su clave de elector a partir de la combinación válida de caracteres. Si la clave no existe o no es vigente, se le notificará.
- El sistema debe poder recibir los datos relacionados a firmas físicas, bajo los criterios que contempla la ley actualmente, e integrarlas al conteo global.
- La administración no se hará responsable el mal uso o manejo de datos personales, a los que no podrá acceder. El promotor será el único responsable legal sobre estos datos, quien ya habrá iniciado una solicitud formal ante las autoridades electorales y generado derechos y obligaciones sobre los datos a recolectar.
- El sistema debe garantizar cumplir con la normatividad correspondiente en el manejo de datos personales, incluido lo referentes al uso de servidores en el extranjero. 
- El sistema debe garantizar un funcionamiento seguro, robusto y sostenible para argumentar su uso frente a las autoridades electorales.
- Los promotores que hayan habilitado el modo brigadista abierto para su iniciativa podrán consultar las firmas digitales recolectadas por cada una y contactarlos en caso de alguna aclaración o anomalía. 

### Componentes oportunos (*nice to have*) 👍🏼 ###
- El sistema podría adecuarse a la legislación local de cada estado para que cada promotor pueda recopilar y exportar firmas digitales en el formato definido por su autoridad electoral local. 
