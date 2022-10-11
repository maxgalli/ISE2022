FROM python:3.9
RUN apt update && apt install libpq-dev python3-dev gcc -y 
RUN python -m pip install --upgrade pip && pip3 install jupyter ipython-sql psycopg2  
RUN jupyter notebook --generate-config
RUN echo "c.NotebookApp.token = ''" >> $HOME/.jupyter/jupyter_notebook_config.py
RUN echo "c.NotebookApp.password = u''" >> $HOME/.jupyter/jupyter_notebook_config.py
CMD jupyter notebook --allow-root  --ip 0.0.0.0 --no-browser --port 8888


