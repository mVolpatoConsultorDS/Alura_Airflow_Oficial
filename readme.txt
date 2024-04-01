##bajar archivo http
curl -O https://caelum-online-public.s3.amazonaws.com/2928-transformacao-manipulacao-dados/dados_vendas_clientes.json

#run program
python3 [program_name].py

source .venv/bin/activate

#Crear ambiente python: python3 -m venv venv
Ativar ambiente: source venv/bin/activate
Desactivar: deactivate 

Verificar los pacotes instalados:  pip freeze
pip freeze > requirements.txt

##Install Air Flow en la carpeta 
pip install apache-airflow

pip install 'apache-airflow==2.3.2' --constraint "https://raw.githubusercontent.com/apache/airflow/constraints-2.3.2/constraints-3.9.txt"

python3.9 -m venv venv
source venv/bin/activate
AIRFLOW_VERSION=2.3.2
PYTHON_VERSION=3.9
CONSTRAINT_URL="https://raw.githubusercontent.com/apache/airflow/constraints-${AIRFLOW_VERSION}/constraints-${PYTHON_VERSION}.txt"
pip install "apache-airflow[postgres,celery,redis]==${AIRFLOW_VERSION}" --constraint "${CONSTRAINT_URL}"
export AIRFLOW_HOME=$(pwd)/airflow_pipeline
airflow standalone





execute: 
export AIRFLOW_HOME=/Users/miltonvolpato/Google\ Drive/Alura/Alura_Airflow
airflow standalone

user: admin
pass: Caso você não consiga identificar a senha, é possível encontrá-la na pasta de execução do Airflow, 
no arquivo chamado "standalone_admin_password.txt".

airflow users delete -u admin
airflow users create --username admin --firstname admin --lastname admin --role Admin --email admin
