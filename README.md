# cocolabs_chatbot

#Validar que todo este en orden

1. rasa data validate

#Entrenar rasa (Siempre hacerlo cuando se realicen cambios)
#Solo es necesario el rasa train, lo demas es para nombrar el modelo y es opcional

2.  - Si deseas registrar el modelo con un nombre:

      - rasa train --fixed-model-name contact_botho

    - Si deseas registrar el modelo sin un nombre:
      - rasa train

#Ejecutar 2. - En consola:
_ rasa shell - Para identificar intents en consola pero no probar las stories:
_ rasa shell nlu - En api: \* rasa run --enable-api

# Cargar a digital ocean

3.  1. Instalar:

       - doctl auth switch --context cocolabs
       - helm install --namespace chatbots --values rasa-values.yml cocolabs-chatbot rasa/rasa

       - helm uninstall cocolabs-chatbot --namespace chatbots (Para eliminar)

    2. Cargar:
       - helm upgrade --namespace chatbots --reuse-values -f rasa-values.yml cocolabs-chatbot rasa/rasa
