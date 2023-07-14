FROM arm64v8/python:3.9 as builder  
WORKDIR /app 
COPY . . 
RUN pip install mkdocs mkdocs-material && mkdocs build 

FROM arm64v8/nginx as deploy 
COPY --from=builder /app/site/ /usr/share/nginx/html/ 
EXPOSE 80