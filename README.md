# Hoser Frontend

## Getting Started
Install the frontend for development (only tested with npm 6.14.8)
```
npm install
```

Compile and run development server with hot-reloads
```
npm run serve
```

Lint and fix files
```
npm run lint
```

## Production
For production, planning to run as containerized 12-Factor app. 

Compile and minify for production outside of container using:
```
npm run build
```

Or, build production image
```
docker build -t hoser-io/hoser-fe .
```

Run production container:
```
docker run -p 8080:80 --rm hoser-io/hoser-fe
```
