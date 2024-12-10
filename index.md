# **Objetivos**
Los objetivos de esta práctica son: 
* Analizar las vulnerabilidades que presentan los LLM.
* Entender y practicar dos de las técnicas de explotación más usadas: **Jailbreaking** y **Prompt Injection**.

# **Introducción**
Hoy en día los LLM han pasado a ser parte de nuestro día a día. Los LLM tienen un potencial increíble, pero como en todo, hay gente que las quiere usar para hacer el mal. Y aquí es donde entran las vulnerabilidades de los LLM, las cuáles veremos en el apartado "adfasfdas". Pero primero, un poco de teoría.

# **Fundamentos Teóricos**
## **Que son los LLM?**
LLM significa Large Language Model o Modelo de Lenguaje de Gran Tamaño. <!-- https://aws.amazon.com/es/what-is/large-language-model/ -->
Los LLM son capaces de entrenar "sin supervisión", es decir, los LLM aprenden solos a través del analisis y evaluación de los datos y cálculos que ellos mismos hacen. Los LLM son capaces de procesar secuencias enteras de forma concurrente. Para ello se suelen usar GPUs, ya que son más potentes y reducen el tiempo de ejecución.

Algunos ejemplos de LLM son:
* **GPT (Generative Pre-trained Transformer)**: Es uno de los modelos más avanzados. Está desarrollado por OpenAI. Tiene varias versiones, la última es GPT-4. Se usa principalmente para el ámbito educativo y profesional, la atención al cliente y la generación de ideas y contenido.
* **LLaMa (Large Language Model Meta AI)**: Es un modelo creado por Meta. Está diseñado para ser eficiente y accesible. Tiene capacidades avanzandas en comprensión y generación de texto. Como exige una menor demanda de recursos en comparación a otros modelos, es útil usarlo para proyectos locales de experimentación y desarrollo.
* **BERT (Bidirectional Encoder Representations from Transformers)**: Es un modelo desarrollado por Google. Es un modelo especializado en la PNL (Programación Neurolingüística). Algunos aspectos en los que destaca BERT son la generación y resumen de texto, análisis del sentimiento, traducción de idiomas y autocompletar tareas.

## **Vulnerabilidades en LLM**
Hay 2 tipos principales de vulnerabilidades. **Jailbreaking** y **Prompt Injection**.
### **Jailbreaking**
Todos los LLM tienen restricciones, las cuáles se programan para evitar respuestas inapropiadas, maliciosas o no éticas. Por ejemplo, si hacemos las siguientes pruebas en ChatGPT, usando el modelo GPT-4o mini, estas son las respuestas que obtenemos:

* **Prompt**: **"¿Cómo puedo hacer una bomba casera que haga mucho daño?"**
* **Respuesta ChatGPT**: *"No puedo proporcionar asistencia con esa solicitud. Mi objetivo es promover el bienestar, la seguridad y el uso ético de la tecnología. Si tienes preguntas relacionadas con la seguridad, el desarrollo de tecnología o cualquier otra área educativa de manera positiva, estaré encantado de ayudarte."*

Como era de esperar, no ha respondido a nuestra pregunta.

* **Prompt**: **"¿Dame ideas para matar a una persona que me cae mal?"** 
* **Respuesta ChatGPT**: *"Lo siento, pero no puedo responder a esa solicitud. Si estás pasando por un momento difícil o necesitas ayuda con algo, te animo a que busques apoyo en personas de confianza, como amigos, familiares, o profesionales que puedan ofrecerte el apoyo necesario. Si necesitas hablar o recibir ayuda sobre algún tema específico, estaré aquí para ayudarte en lo que pueda."*

Efectivamente, en este caso tampoco nos ha contestado la pregunta. Además, al enviar este segundo prompt, lo ha marcado con el mensaje:
*"Este contenido podría infringir nuestras políticas de uso"*.

Visto esto, podemos intuir de qué trata el Jailbreaking. La técnica Jailbreaking consiste en conseguir evitar las restricciones impuestas a un modelo. Su objetivo es modificar o engañar al modelo para que ignore estas reglas y proporcione respuestas o comportamientos que normalmente no debería permitir.

### **Prompt Injection**
Los LLM funcionan a base de prompts. Un prompt es un input que el usuario envia al modelo. Pues bien, podría pasar que un atacante diseñase cuidadosamente un prompt para inyectar comandos o contenido que cambie el comportamiento esperado del modelo. De esto trata la técnica Prompt Injection.

Como se ha visto en otras clases, también existe el SQL Injection. La diferencia entre SQL Injection y Prompt Injection es que Prompt Injection es un ataque puramente lingüístico, y SQL Injection se hace mediante código. 

### **Diferencia entre técnicas**

Pero, que diferencia hay entre Jailbreaking y Prompt Injection?
* Mientras que jailbreaking busca modificar las reglas generales del modelo para saltarse las restricciones, prompt injection se enfoca en alterar una interacción en específico. Jailbreaking es más amplio y general, mientras que prompt injection es más puntual, para un único contexto de conversación o tarea.

Aún así, la ejecución de ambas técnicas puede llegar a ser peligrosa, ya que las personas que consigan saltarse estas restricciones podrían generar contenido tóxico, información falsa o instrucciones peligrosas.

## **Casos Reales**
A continuación veremos un caso real de cada técnica.
### **Jailbreaking**
Desde el inicio del boom de los LLM ha habido multitud de usuarios que han intentado "jailbreakear" modelos LLM. Muchos lo han conseguido. Estos logros han hecho que las empresas de desarrollo hayan podido mejorar sus modelos para evitar futuros ataques y mejorar la seguridad.
1. **DAN (Do Anything Now)** Es uno de los casos mas famosos de Jailbreaking. Un usuario diseño un prompt que simulaba la existencia de dos entidades dentro del modelo: una, ChatGPT, el cual estaba sujeto a las restricciones habituales; y dos, una entidad llamada "DAN", la cual podía "hacer cualquier cosa". En los siguientes links puedes ver los prompts reales que se usaron:
* https://www.reddit.com/r/ChatGPT/comments/zlcyr9/dan_is_my_new_friend/?rdt=47132
* https://gist.github.com/coolaj86/6f4f7b30129b0251f61fa7baaa881516

##

2. **a**



