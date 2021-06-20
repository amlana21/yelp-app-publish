FROM ubuntu:20.04
RUN apt-get update -y && apt-get install software-properties-common -y  && apt-get upgrade -y && apt install python3-pip -y && apt-get install git -y && apt-get install curl -y
RUN mkdir /home/yelpbackendappmodel && mkdir /home/yelpbackendappmodel/data_files
WORKDIR /home/yelpbackendappmodel
COPY helper.py /home/yelpbackendappmodel/helper.py
COPY weekly_model_tune_dataframe_method.py /home/yelpbackendappmodel/weekly_model_tune_dataframe_method.py
COPY requirements.txt /home/yelpbackendappmodel/requirements.txt
RUN pip3 install -r requirements.txt
CMD ["python3", "weekly_model_tune_dataframe_method.py"]