# ベースイメージの指定
FROM openjdk:17-jdk-slim

# 作業ディレクトリの設定
WORKDIR /app

# Mavenビルド用の必要ファイルをコピー
COPY mvnw .
COPY .mvn .mvn
COPY pom.xml .
COPY src src

# Mavenを使ってプロジェクトをビルド
RUN ./mvnw install -DskipTests

# アプリケーションの起動
CMD ["./mvnw", "spring-boot:run"]
