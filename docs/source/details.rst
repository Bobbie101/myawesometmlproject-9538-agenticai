[myawesometmlproject-9538-agenticai] Details
============================

Generated On: 2026-05-15 04:45:05 UTC

TML Solution DAG Parameters' Details: User Chosen Parametets
----------------------------

STEP 1: Get TML Core Params: `tml_system_step_1_getparams_dag <https://github.com/Bobbie101/raspberrypi/tree/main/tml-airflow/dags/tml-solutions/myawesometmlproject-9538/tml_system_step_1_getparams_dag-myawesometmlproject-9538.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - solutionname
     - myawesometmlproject-9538-agenticai
   * - solutiontitle
     - Marine IOT Detector
   * - solutiondescription
     - This is an awesome real-time solution built by TSS
   * - brokerhost
     - 127.0.0.1
   * - brokerport
     - 9092
   * - cloudusername
     - None
   * - ingestdatamethod
     - LOCALFILE
 
STEP 2: Create Kafka Topics: `tml_system_step_2_kafka_createtopic_dag <https://github.com/Bobbie101/raspberrypi/tree/main/tml-airflow/dags/tml-solutions/myawesometmlproject-9538/tml_system_step_2_kafka_createtopic_dag-myawesometmlproject-9538.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - companyname
     - Otics
   * - myname
     - Bobbie
   * - myemail
     - Bobbie.Williams
   * - mylocation
     - Toronto
   * - replication
     - 1
   * - numpartitions
     - 1
   * - enabletls
     - 1
   * - microserviceid
     - 
   * - raw_data_topic
     - iot-raw-data
   * - preprocess_data_topic
     - iot-preprocess,iot-preprocess2
   * - ml_data_topic
     - ml-data
   * - prediction_data_topic
     - prediction-data

STEP 3: `Produce to Kafka Topics <https://github.com/Bobbie101/raspberrypi/tree/main/tml-airflow/dags/tml-solutions/myawesometmlproject-9538/tml_read_LOCALFILE_step_3_kafka_producetotopic_dag-myawesometmlproject-9538.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - PRODUCETYPE
     - LOCALFILE
   * - inputfile
     - 
   * - TOPIC
     - iot-raw-data
   * - PORT
     - _5050
   * - IDENTIFIER
     - TML solution,
   * - HTTPADDR
     - https://
   * - FROMHOST
     - ('0ae8826511b0', '172.17.0.2')
   * - TOHOST
     - 0.0.0.0
   * - CLIENTPORT
     - Not Applicable
   * - TSS_CLIENTPORT
     - Not Applicable
   * - TML_CLIENTPORT
     - Not Applicable
   * - docfolder
     - mylogs,mylogs2
   * - doctopic
     - rtms-stream-mylogs,rtms-stream-mylogs2
   * - chunks
     - 3000
   * - docingestinterval
     - 0

STEP 4: Preprocesing Data: `tml-system-step-4-kafka-preprocess-dag <https://github.com/Bobbie101/raspberrypi/tree/main/tml-airflow/dags/tml-solutions/myawesometmlproject-9538/tml_system_step_4_kafka_preprocess_dag-myawesometmlproject-9538.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - raw_data_topic
     - iot-raw-data
   * - preprocess_data_topic
     - iot-preprocess,iot-preprocess2
   * - preprocessconditions
     - 
   * - delay
     - 70
   * - maxrows
     - 800
   * - array
     - 0
   * - saveasarray
     - 1
   * - topicid
     - -999
   * - rawdataoutput
     - 1
   * - asynctimeout
     - 120
   * - timedelay
     - 0
   * - preprocesstypes
     - anomprob,trend,avg
   * - pathtotmlattrs
     - --pathtotmlattrs--
   * - identifier
     - IoT device performance and failures
   * - jsoncriteria
     - uid=metadata.dsn,filter:allrecords~subtopics=metadata.property_name~values=datapoint.value~identifiers=metadata.display_name~datetime=datapoint.updated_at~msgid=datapoint.id~latlong=lat:long

STEP 4a: Preprocesing Data: `tml-system-step-4a-kafka-preprocess-dag <https://github.com/Bobbie101/raspberrypi/tree/main/tml-airflow/dags/tml-solutions/myawesometmlproject-9538/tml_system_step_4a_kafka_preprocess_dag-myawesometmlproject-9538.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - raw_data_topic
     - --raw_data_topic1--
   * - preprocess_data_topic
     - --preprocess_data_topic1--
   * - preprocessconditions
     - --preprocessconditions1--
   * - delay
     - --delay1--
   * - maxrows
     - --maxrows1--
   * - array
     - --array1--
   * - saveasarray
     - --saveasarray1--
   * - topicid
     - --topicid1--
   * - rawdataoutput
     - --rawdataoutput1--
   * - asynctimeout
     - --asynctimeout1--
   * - timedelay
     - --timedelay1--
   * - preprocesstypes
     - --preprocesstypes1--
   * - pathtotmlattrs
     - --pathtotmlattrs1--
   * - identifier
     - --identifier1--
   * - jsoncriteria
     - --jsoncriteria1--

STEP 4b: Preprocesing Data: `tml-system-step-4b-kafka-preprocess-dag <https://github.com/Bobbie101/raspberrypi/tree/main/tml-airflow/dags/tml-solutions/myawesometmlproject-9538/tml_system_step_4b_kafka_preprocess_dag-myawesometmlproject-9538.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - raw_data_topic
     - --raw_data_topic2--
   * - preprocess_data_topic
     - --preprocess_data_topic2--
   * - preprocessconditions
     - --preprocessconditions2--
   * - delay
     - --delay2--
   * - maxrows
     - --maxrows2--
   * - array
     - --array2--
   * - saveasarray
     - --saveasarray2--
   * - topicid
     - --topicid2--
   * - rawdataoutput
     - --rawdataoutput2--
   * - asynctimeout
     - --asynctimeout2--
   * - timedelay
     - --timedelay2--
   * - preprocesstypes
     - --preprocesstypes2--
   * - pathtotmlattrs
     - --pathtotmlattrs2--
   * - identifier
     - --identifier2--
   * - jsoncriteria
     - --jsoncriteria2--

STEP 4c: Preprocesing Data: `tml-system-step-4c-kafka-preprocess-dag  <https://github.com/Bobbie101/raspberrypi/tree/main/tml-airflow/dags/tml-solutions/myawesometmlproject-9538/tml_system_step_4c_kafka_preprocess_dag-myawesometmlproject-9538.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - raw_data_topic
     - --raw_data_topic3--
   * - preprocess_data_topic
     - --preprocess_data_topic3--
   * - delay
     - --delay3--
   * - maxrows
     - --maxrows3--
   * - array
     - --array3--
   * - saveasarray
     - --saveasarray3--
   * - topicid
     - --topicid3--
   * - rawdataoutput
     - --rawdataoutput3--
   * - asynctimeout
     - --asynctimeout3--
   * - timedelay
     - --timedelay3--
   * - searchterms
     - --rtmssearchterms--
   * - rtmsstream
     - --rtmsstream--
   * - identifier
     - --identifier3--
   * - rememberpastwindows
     - --rememberpastwindows--
   * - patternwindowthreshold
     - --patternwindowthreshold--
   * - localsearchtermfolder
     - --localsearchtermfolder--
   * - localsearchtermfolderinterval
     - --localsearchtermfolderinterval--
   * - rtmsscorethreshold
     - --rtmsscorethreshold--
   * - rtmsscorethresholdtopic
     - --rtmsscorethresholdtopic--
   * - attackscorethreshold
     - --attackscorethreshold--
   * - attackscorethresholdtopic
     - --attackscorethresholdtopic--
   * - patternscorethreshold
     - --patternscorethreshold--
   * - patternscorethresholdtopic
     - --patternscorethresholdtopic--
   * - rtmsfoldername
     - --rtmsfoldername--
   * - rtmsmaxwindows
     - --rtmsmaxwindows--
   * - RTMS Output Github Link
     - `Output Data URL <--rtmsoutputurl-->`_

STEP 5: Entity Based Machine Learning : `tml-system-step-5-kafka-machine-learning-dag <https://github.com/Bobbie101/raspberrypi/tree/main/tml-airflow/dags/tml-solutions/myawesometmlproject-9538/tml_system_step_5_kafka_machine_learning_dag-myawesometmlproject-9538.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - preprocess_data_topic
     - iot-preprocess,iot-preprocess2
   * - ml_data_topic
     - ml-data
   * - modelruns
     - --modelruns--
   * - offset
     - -1
   * - islogistic
     - --islogistic--
   * - networktimeout
     - --networktimeout--
   * - modelsearchtuner
     - --modelsearchtuner--
   * - processlogic
     - --processlogic--
   * - dependentvariable
     - --dependentvariable--
   * - independentvariables
     - --independentvariables--
   * - rollbackoffsets
     - --rollbackoffsets--
   * - topicid
     - -999
   * - consumefrom
     - --consumefrom--
   * - fullpathtotrainingdata
     - --fullpathtotrainingdata--
   * - transformtype
     - --transformtype--
   * - sendcoefto
     - --sendcoefto--
   * - coeftoprocess
     - --coeftoprocess--
   * - coefsubtopicnames
     - --coefsubtopicnames--
   * - ML Output Github Link
     - `Output Data URL <--mloutputurl-->`_

STEP 6: Entity Based Predictions: `tml-system-step-6-kafka-predictions-dag <https://github.com/Bobbie101/raspberrypi/tree/main/tml-airflow/dags/tml-solutions/myawesometmlproject-9538/tml_system_step_6_kafka_predictions_dag-myawesometmlproject-9538.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - preprocess_data_topic
     - iot-preprocess,iot-preprocess2
   * - ml_prediction_topic
     - --ml_prediction_topic--
   * - streamstojoin
     - --streamstojoin--
   * - inputdata
     - --inputdata--
   * - consumefrom
     - --consumefrom2--
   * - offset
     - -1
   * - delay
     - 70
   * - usedeploy
     - --usedeploy--
   * - networktimeout
     - --networktimeout--
   * - maxrows
     - 800
   * - topicid
     - -999
   * - pathtoalgos
     - --pathtoalgos--

STEP 7: Real-Time Visualization: `tml-system-step-7-kafka-visualization-dag <https://github.com/Bobbie101/raspberrypi/tree/main/tml-airflow/dags/tml-solutions/myawesometmlproject-9538/tml_system_step_7_kafka_visualization_dag-myawesometmlproject-9538.py>`_
^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - vipervizport
     - 6060
   * - topic
     - iot-preprocess,iot-preprocess2
   * - dashboardhtml
     - dashboard.html
   * - secure
     - 1
   * - offset
     - -1
   * - append
     - 0
   * - chip
     - arm64
   * - rollbackoffset
     - 400

STEP 8: `tml_system_step_8_deploy_solution_to_docker_dag <https://github.com/Bobbie101/raspberrypi/tree/main/tml-airflow/dags/tml-solutions/myawesometmlproject-9538/tml_system_step_8_deploy_solution_to_docker_dag-myawesometmlproject-9538.py>`_
^^^^^^^^^^^^^^^^^^^^^
.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - Docker Container
     - --dockercontainer--
   * - Docker Run Command
     - --dockerrun--

STEP 9: `tml_system_step_9_privategpt_qdrant_dag <https://github.com/Bobbie101/raspberrypi/tree/main/tml-airflow/dags/tml-solutions/myawesometmlproject-9538/tml_system_step_9_privategpt_qdrant_dag-myawesometmlproject-9538.py>`_
^^^^^^^^^^^^^^^^^^^^^
.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - PrivateGPT Container
     - --pgptcontainername--
   * - PrivateGPT Run Command
     - --privategptrun--
   * - Qdrant Container
     - --qdrantcontainer--
   * - Qdrant Run Command
     - --qdrantrun--
   * - Consumefrom
     - --consumefrom--
   * - pgpt_data_topic
     - --pgpt_data_topic--
   * - offset
     - -1
   * - rollbackoffset
     - 400
   * - topicid
     - -999
   * - enabletls
     - 1
   * - partition
     - --partition--
   * - prompt
     - --prompt--
   * - context
     - --context--
   * - jsonkeytogather
     - --jsonkeytogather--
   * - keyattribute
     - --keyattribute--
   * - keyprocesstype
     - --keyprocesstype--
   * - vectordbcollectionname
     - --vectordbcollectionname--
   * - concurrency
     - --concurrency--
   * - CUDA_VISIBLE_DEVICES
     - --cuda--
   * - pgpthost
     - --pgpthost--
   * - pgptport
     - --pgptport--
   * - hyperbatch
     - --hyperbatch--
   * - docfolder
     - --docfolder--
   * - docfolderingestinterval
     - --docfolderingestinterval--
   * - useidentifierinprompt
     - --useidentifierinprompt--
   * - searchterms
     - --searchterms--
   * - streamall
     - --streamall--
   * - temperature
     - --temperature--
   * - vectorsearchtype
     - --vectorsearchtype--
   * - llm
     - --llmmodel--
   * - embedding
     - --embedding--
   * - vectorsize
     - --vectorsize--
   * - contextwindowsize
     - --contextwindowsize--
   * - vectordimension
     - --vectordimension--
   * - mitrejson
     - --mitrejson--

STEP 9b: `tml_system_step_9b_agenticai_dag <https://github.com/Bobbie101/raspberrypi/tree/main/tml-airflow/dags/tml-solutions/myawesometmlproject-9538/tml_system_step_9b_agenticai_dag-myawesometmlproject-9538.py>`_
^^^^^^^^^^^^^^^^^^^^^
.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - rollbackoffset
     - 5
   * - ollama-model
     - llama3.1
   * - deletevectordbcount
     - 10
   * - vectordbpath
     - /rawdata/vectordb
   * - temperature
     - 0.1
   * - topicid
     - -999
   * - enabletls
     - 1
   * - partition
     - -1
   * - vectordbcollectionname
     - tml-llm-model-v2
   * - ollamacontainername
     - maadsdocker/tml-privategpt-with-gpu-nvidia-amd64-llama3-tools
   * - mainip
     - http://127.0.0.1
   * - mainport
     - 11434
   * - embedding
     - nomic-embed-text
   * - agenttopic
     - 
   * - agents_topic_prompt
     - 
<consumefrom - topic agent will monitor:prompt you want for the agent to answer->>consumefrom - topic2 agent will monitor<<-prompt you want for the agent to answer>

   * - teamlead_topic
     - 
   * - teamleadprompt
     - 
Enter the prompt for the Team lead agent

   * - supervisor_topic
     - 
   * - supervisorprompt
     - 
   * - agenttoolfunctions
     - 
tool_function:agent_name:system_prompt
   * - agent_team_supervisor_topic
     - 
   * - concurrency
     - 2
   * - CUDA_VISIBLE_DEVICES
     - 0
   * - contextwindow
     - 10000
   * - localmodelsfolder
     - /rawdata/ollama

STEP 10: `tml_system_step_10_documentation_dag <https://github.com/Bobbie101/raspberrypi/tree/main/tml-airflow/dags/tml-solutions/myawesometmlproject-9538/tml_system_step_10_documentation_dag_myawesometmlproject-9538_tml-multi-agenticai-iot-3f10-myawesometmlproject-9538.py>`_
^^^^^^^^^^^^^^^^^^^^^
.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - Solution Documentation URL
     - https://myawesometmlproject-9538-agenticai.readthedocs.io
