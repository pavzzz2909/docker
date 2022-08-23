FROM python:3.8

WORKDIR /crud_3-2

COPY ./crud_3-2 /crud_3-2

RUN pip install -r /crud_3-2/requirements.txt

ENV SECRET_KEY django-insecure-nw^y+m^wmxza1asgk+)!ua2qx9)g+#v=6%76-9i8i(6eqiw94j
ENV DEBUG 1

RUN python manage.py migrate

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "stocks_products.wsgi"]
