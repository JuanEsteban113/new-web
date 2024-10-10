from flask import Flask
import random

app = Flask(__name__)

datos = ["Efecto Dunning-Kruger Muchas personas sobreestiman su comprensión de la tecnología lo que puede llevar a una dependencia sin una verdadera comprensión de cómo funciona Esto puede hacer que sean reacias a cambiar a nuevas herramientas"

"FOMO Tecnológico El miedo a quedarse atrás impulsa a muchos a adoptar nuevas tecnologías rápidamente creando una dependencia sin una evaluación crítica de su utilidad",

"Obsolescencia Programada Muchas tecnologías están diseñadas para volverse obsoletas o menos eficientes con el tiempo lo que fomenta la dependencia de actualizaciones y nuevos modelos",

"Efecto Lock-in Una vez que las empresas adoptan un sistema particular a menudo es costoso y complicado cambiar a otro creando un fenómeno de lock-in donde se sienten atrapadas",

"Disminución de Habilidades Con el aumento de herramientas tecnológicas algunas habilidades manuales o cognitivas están disminuyendo Por ejemplo la calculadora ha reducido la práctica de las matemáticas mentales",

"Dependencia de Internet En dos mil veintiuno un informe indicó que más del cuatro punto nueve mil millones de personas en el mundo eran usuarios activos de Internet lo que resalta la dependencia de la conectividad para la comunicación trabajo y acceso a la información",

"Impacto en la Salud Mental Estudios han mostrado que la dependencia excesiva de la tecnología puede contribuir a problemas de salud mental como ansiedad y depresión especialmente entre jóvenes",

"Uso de Asistentes Virtuales La dependencia de asistentes virtuales como Siri Alexa o Google Assistant ha crecido rápidamente Se estima que más del cincuenta por ciento de las búsquedas en Internet se realizarán mediante voz para dos mil veinticinco",

"La Brecha Digital La dependencia de la tecnología puede exacerbar la desigualdad ya que aquellos sin acceso a dispositivos y conexión a Internet quedan en desventaja en educación empleo y servicios",

"Sustitución de Interacciones Humanas La dependencia de plataformas de mensajería y redes sociales ha cambiado la forma en que nos comunicamos a menudo reemplazando interacciones cara a cara con interacciones digitales"]
@app.route("/")
def hello_world():
    return "<h1>hola mundo</h1><a href=/datoss>IR A  MIS DATOS RANDOM</A>"

@app.route("/datoss")
def datoss():
    return f'<p>{random.choice(datos)}</p>'

app.run(debug=True)

