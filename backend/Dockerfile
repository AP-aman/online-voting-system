FROM eclipse-temurin:17-jdk

WORKDIR /app

COPY . .

RUN chmod +x mvnw
RUN ./mvnw clean package -DskipTests

EXPOSE 8080

# ✅ FORCE PORT from Render
CMD ["sh", "-c", "java -Dserver.port=$PORT -jar target/*.jar"]