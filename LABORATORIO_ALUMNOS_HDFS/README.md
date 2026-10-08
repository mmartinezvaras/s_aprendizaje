# Laboratorio inicial del alumno: Hadoop/HDFS

Este paquete contiene únicamente los archivos necesarios para la primera sesión. Las prácticas, los datos de ejemplo, las configuraciones de Kafka, Hive, Streams y las soluciones se entregarán en las clases correspondientes.

## Arranque

Desde esta carpeta:

    chmod +x lab
    docker compose config --quiet
    docker compose build namenode
    docker compose up -d namenode dn1 dn2 dn3
    docker compose ps
    ./lab h dfsadmin -report

La comprobación correcta muestra:

    Live datanodes (3)

La interfaz del NameNode está disponible en http://localhost:9870.

## Parar el laboratorio

Para parar los contenedores conservando los volúmenes:

    docker compose stop

No ejecutes \`docker compose down -v\` salvo que el profesor lo indique: elimina los volúmenes y borra el estado de HDFS.
