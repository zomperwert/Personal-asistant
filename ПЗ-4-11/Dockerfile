FROM python:3.13.3

WORKDIR /app

# Копіюємо тільки необхідні файли
COPY Pipfile Pipfile.lock ./
COPY *.py ./

# Встановлюємо pipenv та залежності
RUN pip install pipenv && \
    pipenv install --system --deploy

# Створюємо папку для даних
RUN mkdir -p /app/data

CMD ["python", "./__main__.py"]