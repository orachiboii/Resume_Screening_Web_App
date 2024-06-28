# Resume_Screening_Web_App

## Starting Stanford CoreNLP Java Server:
1. Downlaod Stanford CoreNLP from https://stanfordnlp.github.io/CoreNLP/download.html
2. cd to the downloaded folder
3. Check if any process running on port 9000: if yes, kill it
   netstat -aof | findstr :9000 (to find the process)
   taskkill /PID 5896 /F (to kill task (eg task number 5896))
4. In cmd, java -mx4g -cp "*" edu.stanford.nlp.pipeline.StanfordCoreNLPServer -annotators "tokenize,ssplit,pos,lemma,parse,sentiment" -port 9000 -timeout 30000
5. Server listening on port 0.0.0.9000

## Starting FastAPI Backend:
1. From main project folder, cd backend
2. In cmd, uvicorn main:app --reload

## Starting React Frontend:
1. From main folder, cd frontend
2. In cmd, npm start
