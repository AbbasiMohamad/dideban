# development guideline


- postgres run command: docker run --name postgres -e POSTGRES_USER=didehban -e POSTGRES_PASSWORD=password -p 5432:5432 -d postgres
- postgres://didehban:password@localhost/didehban?sslmode=disable
- migrate create -seq -ext=.sql -dir=./migrations <migration name>
- migrate -path=./migrations -database=$DIDEHBAN_DB_DSN up  | or
- migrate -path=./migrations -database=postgres://didehban:password@localhost/didehban?sslmode=disable up