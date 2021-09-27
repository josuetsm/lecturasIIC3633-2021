# Lectura 6

#### Texto: Zhang, S., Yao, L., Sun, A., & Tay, Y. (2019). Deep learning based recommender system: A survey and new perspectives. ACM Computing Surveys (CSUR), 52(1), 1-38.

El texto analiza los principales aportes de los sistemas recomendadores basados en modelos de Deep learning (DL). Si bien este tipo de modelos son conocidos por alcanzar mejores rendimientos que los modelos clásicos en métricas de predicción, las principales ventajas identificadas por los autores giran en torno a la posibilidad de poder entrenar un modelo End-to-end completamente diferenciable con datos provenientes de dominios diversos (texto, imagen, audio, interacciones, etc.), además de tener una mayor capacidad de generalizar en vez de memorizar a través de aprender representaciones apropiadas. Adicionalmente identifican ciertas debilidades de estos modelos, tales como la demandante cantidad de datos que necesitan los modelos para poder entrenar sus parámetros, como los problemas de interpretabilidad.

De todos los modelos revisados, el que llamó más mi atención fue el Collaborative Denoising Auto-Encoder (CDAE) debido a que la estrategia para poder llenar los vacíos de la matriz usuario-ítem me pareció bastante ingeniosa. En este modelo corrompen esta matriz, introduciendo un ruido de distribución gaussiana y entrenan el modelo para que elimine ese ruido, aprendiendo en el proceso las casillas vacías de la matriz usuario-ítem.

Otro aspecto que me pareció interesante fue el modelo de Lei et al. (2016), quienes proponen entrenar su modelo en tripletas de un usuario u, una imagen positiva I+ y una imagen negativa I-. En general, encontré que esta estrategia sigue un poco la línea del modelo BPR (Rendle et al., 2009) para feedback implícito, debido a que lo que importa es predecir correctamente cuál es la imagen más cercana al usuario.

Finalmente, debo destacar que, a pesar de que mi tesis no esté enforcada en sistemas recomendadores, en general este tipo de artículos me ha servido para ir explorando nuevas ideas. Con la lectura de la semana pasada pude implementar un modelo de Asymmetric Factor Modelo (Paterek, 2007) para poder disminuir la cantidad de parámetros de un modelo y esta semana estoy pensando en probar con un modelo Auto-encoder que permita aprender tópicos a partir de una matriz de documento-palabra.

* Chenyi Lei, Dong Liu, Weiping Li, Zheng-Jun Zha, and Houqiang Li. (2016). Comparative Deep Learning of Hybrid Representations for Image Recommendations. In *Proceedings of the IEEE Conference on Computer Vision and Pa.ern Recognition*. 2545–2553.
* Rendle, S., Freudenthaler, C., Gantner, Z., & Schmidt-Thieme, L. (2009). BPR: Bayesian personalized ranking from implicit feedback. In *Proceedings of the Twenty-Fifth Conference on Uncertainty in Artificial Intelligence* (pp. 452-461). AUAI Press.
* Paterek. A., (2007). Improving regularized singular value decomposition for collaborative filtering. *Proceedings of KDD Cup and Workshop*.
