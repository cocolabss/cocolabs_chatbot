# cocolabs_chatbot

#Validar que todo este en orden
1. rasa data validate

#Entrenar rasa (Siempre hacerlo cuando se realicen cambios)
#Solo es necesario el rasa train, lo demas es para nombrar el modelo y es opcional
2. 
    - Si deseas registrar el modelo con un nombre:
    * rasa train --fixed-model-name contact_bot

    - Si deseas registrar el modelo sin un nombre:
    * rasa train

#Ejecutar
2. 
    - En consola:
    * rasa shell

    En api:
    * rasa run --enable-api