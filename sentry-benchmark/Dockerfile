# Используем официальный Go образ
FROM golang:1.21-alpine

# Устанавливаем рабочую директорию
WORKDIR /app

# Копируем go.mod и go.sum
COPY go.mod go.sum ./

# Загружаем зависимости
RUN go mod download

# Копируем исходный код
COPY . .

# Собираем приложение
RUN go build -o main .

# Указываем порт, который будет использоваться контейнером
EXPOSE 8080

# Запускаем приложение
CMD ["./main"]
