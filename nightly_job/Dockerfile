FROM ubuntu:20.04
RUN apt-get update -y && apt-get install software-properties-common -y  && apt-get upgrade -y && apt install python3-pip -y && apt-get install git -y && apt-get install curl -y
RUN mkdir /home/yelpbackendapp && mkdir /home/yelpbackendapp/data_files
WORKDIR /home/yelpbackendapp
COPY helper.py /home/yelpbackendapp/helper.py
COPY nightly_data_process_dataframe.py /home/yelpbackendapp/nightly_data_process_dataframe.py
COPY requirements.txt /home/yelpbackendapp/requirements.txt
RUN pip3 install -r requirements.txt
CMD ["python3", "nightly_data_process_dataframe.py"]