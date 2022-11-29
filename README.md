## PT-BR | INSTALAÇÃO SPARK NO UBUNTU 22.04.1 LTS
## EN | APACHE SPARK INSTALLATION ON UBUNTU 22.04.1 LTS


---

### 📌 Execute os comandos abaixo:

``` sudo apt update && sudo apt -y upgrade ```

``` sudo apt install curl mlocate default-jdk -y  ```

``` wget https://dlcdn.apache.org/spark/spark-3.2.2/spark-3.2.2-bin-hadoop3.2.tgz  ```

``` tar xvf spark spark-3.2.2-bin-hadoop3.2.tgz  ```

``` sudo mv spark-3.2.2-bin-hadoop3.2.tgz /opt/spark  ```

``` sudo gedit ~/.bashrc  ```

Adicionar no final do arquivo:

```
export SPARK_HOME=/opt/spark
export PATH=$PATH:$SPARK_HOME/bin:$bin$SPARK_HOME/sbin
```

``` source /.bashrc  ```

``` start-master.sh  ```

``` /opt/spark/sbin/start-slave.sh spark://localhost:7077 ```

---

## PT-BR | INSTALAÇÃO JUPYTER NOTEBOOK

### 📌 Execute os comandos abaixo:

``` sudo apt update && sudo apt -y upgrade ```

``` sudo apt install python3-pip python3-dev ```

``` sudo -H pip3 install --upgrade pip ```

``` sudo -H pip3 install virtualenv ```

``` mkdir notebook ```

```  cd notebook ```

``` virtualenv jupyterenv ```

``` source jupyterenv/bin/activate ```

``` pip install jupyter ```

``` jupyter notebook ```
