# flask_template

## venv
    python3 -m venv .venv

## install
    pip install flask 

    pip install pymongo

## Html
    <!DOCTYPE html>
    <html lang="ko">
        <head>
            <!-- 다양한 언어를 사용할 수 있도록 UTF-8 을 사용하도록 합니다. -->
            <meta charset="UTF-8"/>
    
            <!-- 반응형으로 동작하게 합니다. -->
            <meta title="viewport" content="width=device-width, initial-scale=1.0"/>
    
            <!-- Bootstrap 을 포함합니다. -->
            <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
            <link href="https://getbootstrap.com/docs/5.3/assets/css/docs.css" rel="stylesheet">
    
            <!-- jQuery 를 포함합니다. -->
            <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
    
            <!-- CSS library 인 Bulma 를 포함합니다. -->
            <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.8.0/css/bulma.min.css"/>
    
            <!-- 텍스트형태로 되어있는 icon 을 쓸 수 있도록 Font awesome 을 포함하빈다. -->
            <script defer src="https://use.fontawesome.com/releases/v6.4.0/js/all.js"></script>
    
            <title>...</title>

            <style>
                
            </style>
    
            
            <script>
              
            </script>
        </head>
    
        <body>
         
        </body>
    </html>
    
## app.py
      from bson import ObjectId
      from pymongo import MongoClient
      
      from flask import Flask, render_template, jsonify, request
      from flask.json.provider import JSONProvider
      
      import json
      import sys
      
      
      app = Flask(__name__)
      
      client = MongoClient('localhost', 27017)
      db = client.dbjungle
    
      @app.route('/')
      def home():
          return render_template('index.html')
          
      if __name__ == '__main__':
        print(sys.executable)
        app.run('0.0.0.0', port=5000, debug=True)



  
