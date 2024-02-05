# 1、**Hello World**
~~~python
print("Hello, World!")  
~~~
官方文档: _https://docs.python.org/3/_
[3.12.1 Documentation (python.org)](https://docs.python.org/zh-cn/3/)
# 2、**变量和数据类型**
~~~python
name = "Alice"  
age = 30  
height = 175.5  
is_student = True  
~~~
官方文档: _https://docs.python.org/3/tutorial/introduction.html#numbers_
# 3、**列表**
~~~python
fruits = ["apple", "banana", "cherry"]  
fruits.append("date")  
print(fruits)  
~~~
官方文档: _https://docs.python.org/3/tutorial/introduction.html#lists_
# 4、**字典**
~~~python
person = {"name": "Alice", "age": 30, "city": "New York"}  
print(person["name"])  
~~~
官方文档: _https://docs.python.org/3/tutorial/datastructures.html#dictionaries_
# 5、**循环**
~~~python
for i in range(1, 6):  
    print(i)  
~~~
官方文档: _https://docs.python.org/3/tutorial/introduction.html#first-steps-towards-programming_
# 6、**条件语句**
~~~python
x = 5  
if x > 10:  
    print("x is greater than 10")  
else:  
    print("x is not greater than 10")  
~~~
官方文档: _https://docs.python.org/3/tutorial/controlflow.html_
# 7、**函数**
~~~python
def greet(name):  
    return f"Hello, {name}!"  
  
message = greet("Alice")  
print(message)  
~~~
官方文档: _https://docs.python.org/3/tutorial/controlflow.html#defining-functions_
# 8、**模块导入**
~~~python
import math  
  
print(math.sqrt(16))  
~~~
官方文档: _https://docs.python.org/3/tutorial/modules.html_
# 9、**异常处理**
~~~python
try:  
    result = 10 / 0  
except ZeroDivisionError:  
    print("Division by zero is not allowed.")  
~~~
官方文档: _https://docs.python.org/3/tutorial/errors.html_
# 10、**文件操作**
~~~python
with open("example.txt", "w") as file:  
    file.write("Hello, File!")  
  
with open("example.txt", "r") as file:  
    content = file.read()  
    print(content)  
~~~
官方文档: _https://docs.python.org/3/tutorial/inputoutput.html_
# 11、**日期和时间**
~~~python
from datetime import datetime  
  
now = datetime.now()  
print(now)  
~~~
官方文档: _https://docs.python.org/3/library/datetime.html_
# 12、**随机数生成**
~~~python
import random  
  
random_number = random.randint(1, 100)  
print(random_number)  
~~~
官方文档: _https://docs.python.org/3/library/random.html_
# 13、**正则表达式**
~~~python
import re
	text = "Hello, 12345"  
	pattern = r'\d+'  
	match = re.search(pattern, text)  
if match:
	print(match.group())  
~~~
官方文档: _https://docs.python.org/3/library/re.html_
# 14、**Web请求**
~~~python
import requests  
  
response = requests.get("https://www.example.com")  
print(response.text)  
~~~
官方文档: _https://docs.python-requests.org/en/master/_
# 15、**CSV文件处理**
~~~python
import csv  
  
with open("data.csv", "w", newline="") as file:  
    writer = csv.writer(file)  
    writer.writerow(["Name", "Age"])  
    writer.writerow(["Alice", 25])  
  
with open("data.csv", "r") as file:  
    reader = csv.reader(file)  
    for row in reader:  
        print(row)  
~~~
官方文档: _https://docs.python.org/3/library/csv.html_
# 16、**JSON处理**
~~~python
import json  
	data = {"name": "Bob", "age": 35}  
	json_data = json.dumps(data)  
	print(json_data)  
~~~
官方文档: _https://docs.python.org/3/library/json.html_
# 17、**爬虫 - BeautifulSoup**
~~~python
from bs4 import BeautifulSoup  
import requests  
  
url = "https://www.example.com"  
response = requests.get(url)  
soup = BeautifulSoup(response.text, "html.parser")  
print(soup.title.text)  
~~~
官方文档: _https://www.crummy.com/software/BeautifulSoup/bs4/doc/_
# 18、**多线程**
~~~python
import threading  
  
def print_numbers():  
    for i in range(1, 6):  
        print(f"Number: {i}")  
  
def print_letters():  
    for letter in "abcde":  
        print(f"Letter: {letter}")  
  
thread1 = threading.Thread(target=print_numbers)  
thread2 = threading.Thread(target=print_letters)  
  
thread1.start()  
thread2.start()  
~~~
官方文档: _https://docs.python.org/3/library/threading.html_
# 23、**数据爬取 - Selenium**
~~~python
from selenium import webdriver  
  
driver = webdriver.Chrome()  
driver.get("https://www.example.com")  
~~~
官方文档: _https://www.selenium.dev/documentation/en/_
# 20、**REST API - Flask**
~~~python
from flask import Flask, jsonify  
  
app = Flask(__name)  
  
@app.route('/api', methods=['GET'])  
def get_data():  
    data = {'message': 'Hello, API!'}  
    return jsonify(data)  
  
if __name__ == '__main__':  
    app.run()  
~~~
官方文档: _https://flask.palletsprojects.com/en/2.1.x/_
# 21、**数据库连接 - SQLite**
~~~python
import sqlite3  
  
conn = sqlite3.connect('mydatabase.db')  
cursor = conn.cursor()  
cursor.execute('CREATE TABLE IF NOT EXISTS users (id INTEGER PRIMARY KEY, name TEXT)')  
conn.commit()  
conn.close()  
~~~
官方文档: _https://www.sqlite.org/docs.html_
# 22、**图像处理 - Pillow**
~~~python
from PIL import Image  
  
img = Image.open('example.jpg')  
img.show()  
~~~
官方文档: _https://pillow.readthedocs.io/en/stable/index.html_
# 23、**图形界面 - Tkinter**
~~~python
import tkinter as tk  
  
root = tk.Tk()  
label = tk.Label(root, text="Hello, GUI!")  
label.pack()  
root.mainloop()  
~~~
官方文档: _https://docs.python.org/3/library/tkinter.html_
# 24、**文本生成 - Faker**
~~~python
from faker import Faker  
  
fake = Faker()  
print(fake.name())  
~~~
官方文档: _https://faker.readthedocs.io/en/master/_
# 25、**加密和解密 - cryptography**
~~~python
from cryptography.fernet import Fernet  
  
key = Fernet.generate_key()  
cipher_suite = Fernet(key)  
text = "Secret message".encode()  
cipher_text = cipher_suite.encrypt(text)  
print(cipher_text)  
~~~
官方文档: _https://cryptography.io/en/latest/_
# 26、**Socket编程**
~~~python
import socket  
  
server_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)  
server_socket.bind(('127.0.0.1', 12345))  
server_socket.listen(5)  
print("Server is listening...")  
  
while True:  
    client_socket, addr = server_socket.accept()  
    print(f"Connection from {addr}")  
    client_socket.send(b"Hello, client!")  
    client_socket.close()  
~~~
官方文档: _https://docs.python.org/3/library/socket.html_
# 27、**并发编程 - threading**
~~~python
import threading  
  
def print  
  
_numbers():  
    for i in range(1, 6):  
        print(f"Number: {i}")  
  
def print_letters():  
    for letter in "abcde":  
        print(f"Letter: {letter}")  
  
thread1 = threading.Thread(target=print_numbers)  
thread2 = threading.Thread(target=print_letters)  
  
thread1.start()  
thread2.start()  
~~~
官方文档: _https://docs.python.org/3/library/threading.html_
# 28、**正则表达式 - re**
~~~python
import re  
  
text = "My phone number is 123-456-7890."  
pattern = r'\d{3}-\d{3}-\d{4}'  
match = re.search(pattern, text)  
if match:  
    print(f"Phone number found: {match.group()}")  
~~~
官方文档: _https://docs.python.org/3/howto/regex.html_
# 29、**REST API - FastAPI**
~~~python
from fastapi import FastAPI  
  
app = FastAPI()  
  
@app.get("/items/{item_id}")  
def read_item(item_id: int, query_param: str = None):  
    return {"item_id": item_id, "query_param": query_param}  
~~~
官方文档: _https://fastapi.tiangolo.com/_
# 30、**数据库连接 - SQLAlchemy**
~~~python
from sqlalchemy import create_engine, Column, Integer, String  
from sqlalchemy.orm import sessionmaker  
from sqlalchemy.ext.declarative import declarative_base  
  
engine = create_engine('sqlite:///mydatabase.db')  
Base = declarative_base()  
  
class User(Base):  
    __tablename__ = 'users'  
    id = Column(Integer, primary_key=True)  
    name = Column(String)  
  
Session = sessionmaker(bind=engine)  
session = Session()  
~~~
官方文档: _https://docs.sqlalchemy.org/en/20/_
# 31、**文本处理 - NLTK**
~~~python
import nltk  
nltk.download('punkt')  
from nltk.tokenize import word_tokenize  
  
text = "This is a sample sentence."  
tokens = word_tokenize(text)  
print(tokens)  
~~~
官方文档: _https://www.nltk.org/_
# 32、**命令行应用 - argparse**
~~~python
import argparse  
  
parser = argparse.ArgumentParser(description='A simple command-line app')  
parser.add_argument('--name', type=str, help='Your name')  
args = parser.parse_args()  
print(f'Hello, {args.name}!')  
~~~
官方文档: _https://docs.python.org/3/library/argparse.html_
# 33、**微服务 - Flask-RESTful**
~~~python
from flask import Flask  
from flask_restful import Resource, Api  
  
app = Flask(__name)  
api = Api(app)  
  
class HelloWorld(Resource):  
    def get(self):  
        return {'message': 'Hello, World!'}  
  
api.add_resource(HelloWorld, '/')  
~~~
官方文档: _https://flask-restful.readthedocs.io/en/latest/_
# 34、**数据处理 - BeautifulSoup**
~~~python
from bs4 import BeautifulSoup  
import requests  
  
url = "https://www.example.com"  
response = requests.get(url)  
soup = BeautifulSoup(response.text, "html.parser")  
print(soup.title.text)  
~~~
官方文档: _https://www.crummy.com/software/BeautifulSoup/bs4/doc/_
# 35、**加密 - hashlib**
~~~python
import hashlib  
  
text = "Secret Password"  
hash_object = hashlib.sha256(text.encode())  
hash_hex = hash_object.hexdigest()  
print(hash_hex)  
~~~
官方文档: _https://docs.python.org/3/library/hashlib.html_
# 36、**数据序列化 - Pickle**
~~~python
import pickle  
  
data = {'name': 'Alice', 'age': 30}  
with open('data.pkl', 'wb') as file:  
    pickle.dump(data, file)  
  
with open('data.pkl', 'rb') as file:  
    loaded_data = pickle.load(file)  
    print(loaded_data)  
~~~
官方文档: _https://docs.python.org/3/library/pickle.html_
# 37、**并行处理 - concurrent.futures**
~~~python
import concurrent.futures  
  
def square(x):  
    return x * x  
  
with concurrent.futures.ThreadPoolExecutor() as executor:  
    results = executor.map(square, [1, 2, 3, 4, 5])  
  
for result in results:  
    print(result)  
~~~
官方文档: _https://docs.python.org/3/library/concurrent.futures.html_
# 38、**网络爬虫 - Scrapy**
~~~python
import scrapy  
  
class MySpider(scrapy.Spider):  
    name = 'example.com'  
    start_urls = ['https://www.example.com']  
  
    def parse(self, response):  
        # 爬取和处理数据  
        pass  
~~~
官方文档: _https://docs.scrapy.org/en/latest/_
# 39、**异步编程 - asyncio**
~~~python
import asyncio  
  
async def hello():  
    await asyncio.sleep(1)  
    print("Hello, Async!")  
  
loop = asyncio.get_event_loop()  
loop.run_until_complete(hello())  
~~~
官方文档: _https://docs.python.org/3/library/asyncio.html_
# 40、**数据分析 - Numpy**
~~~python
import numpy as np  
  
arr = np.array([1, 2, 3, 4, 5])  
print(arr.mean())  
~~~
官方文档: _https://numpy.org/doc/stable/_
# 41、**数据处理 - Pandas**
~~~python
import pandas as pd  
  
data = {'Name': ['Alice', 'Bob', 'Charlie'], 'Age': [25, 30, 35]}  
df = pd.DataFrame(data)  
print(df)  
~~~
官方文档: _https://pandas.pydata.org/docs/_
# 42、**数据可视化 - Matplotlib**
~~~python
import matplotlib.pyplot as plt  
  
x = [1, 2, 3, 4, 5]  
y = [10, 15, 13, 18, 20]  
plt.plot(x, y)  
plt.show()  
~~~
官方文档: _https://matplotlib.org/stable/contents.html_
# 43、**机器学习 - Scikit-Learn**
~~~python
from sklearn.datasets import load_iris  
from sklearn.model_selection import train_test_split  
from sklearn.ensemble import RandomForestClassifier  
  
iris = load_iris()  
X_train, X_test, y_train, y_test = train_test_split(iris.data, iris.target, test_size=0.2)  
clf = RandomForestClassifier(n_estimators=100)  
clf.fit(X_train, y_train)  
~~~
官方文档: _https://scikit-learn.org/stable/documentation.html_
# 44、**机器学习 - Keras**
~~~python
from keras.models import Sequential  
from keras.layers import Dense  
  
model = Sequential()  
model.add(Dense(units=64, activation='relu', input_dim=100))  
model.add(Dense(units=10, activation='softmax'))  
~~~
官方文档: _https://keras.io/guides/_
# 45、**图像处理 - OpenCV**
~~~python
import cv2  
  
image = cv2.imread('image.jpg')  
cv2.imshow('Image', image)  
cv2.waitKey(0)  
cv2.destroyAllWindows()  
~~~
官方文档: _https://docs.opencv.org/master/index.html_
# 46、**数据爬取 - Scrapy**
~~~python
import scrapy  
  
class MySpider(scrapy.Spider):  
    name = 'example.com'  
    start_urls = ['https://www.example.com']  
  
    def parse(self, response):  
        # 爬取和处理数据  
        pass  
~~~
官方文档: _https://docs.scrapy.org/en/latest/_
# 47、**数据分析 - [[seaborn]]**
~~~python
import seaborn as sns  
import matplotlib.pyplot as plt  
  
data = sns.load_dataset("iris")  
sns.pairplot(data, hue="species")  
plt.show()  
~~~
官方文档: _https://seaborn.pydata.org/introduction.html_
![[../../归档/picture/Seaborn数据分析示意图.png]]
# 48、**数据可视化 - Plotly**
~~~python
import plotly.express as px  
  
fig = px.scatter(x=[1, 2, 3, 4], y=[10, 11, 12, 13])  
fig.show()  
~~~
官方文档: _https://plotly.com/python/_
# 49、**自然语言处理 - spaCy**
~~~python
import spacy  
  
nlp = spacy.load('en_core_web_sm')  
doc = nlp("This is a sample sentence.")  
for token in doc:  
    print(token.text, token.pos_)  
~~~
官方文档: _https://spacy.io/usage/spacy-101_
# 50、**机器学习 - XGBoost**
~~~python
import xgboost as xgb  
  
data = xgb.DMatrix('train.csv')  
param = {'max_depth': 3, 'eta': 0.1, 'objective': 'reg:squarederror'}  
model = xgb.train(param, data, 10)  
~~~
官方文档: _https://xgboost.readthedocs.io/en/latest/_
# **Last - 云图**
~~~python
import matplotlib.pyplot as plt  
from wordcloud import WordCloud  
  
# 方面列表和它们的权重  
aspects = {  
    "Hello World": 3,  
    "Variables and Data Types": 4,  
    "Lists": 4,  
    "Dictionaries": 4,  
    "Loops": 4,  
    "Conditional Statements": 4,  
    "Functions": 4,  
    "Module Import": 4,  
    "Exception Handling": 4,  
    "Date and Time": 5,  
    "Random Number Generation": 5,  
    "Regular Expressions": 5,  
    "CSV File Handling": 5,  
    "JSON Handling": 5,  
    "BeautifulSoup": 5,  
    "File Operations": 5,  
    "Multithreading": 5,  
    "Tkinter": 5,  
    "Pandas": 6,  
    "asyncio": 5,  
    "XGBoost": 6,  
    "Matplotlib": 5,  
    "Scikit-Learn": 5,  
    "Selenium": 5,  
    "Flask": 1,  
    "Web Requests": 3,  
    "SQLite": 3,  
    "Pillow": 3,  
    "Numpy": 6,  
    "Faker": 3,  
    "cryptography": 3,  
    "Socket Programming": 3,  
    "threading": 3,  
    "re": 4,  
    "NLTK": 5,  
    "Keras": 7,  
    "OpenCV": 7,  
    "Scrapy": 7,  
    "FastAPI": 3,  
    "SQLAlchemy": 5,  
    "Seaborn": 5,  
    "Plotly": 5,  
    "argparse": 5,  
    "Flask-RESTful": 3,  
    "BeautifulSoup": 3,  
    "spaCy": 6,  
    "hashlib": 5,  
    "Pickle": 5,  
    "concurrent.futures": 5,  
    "Scrapy": 6  
}  
  
# 将方面列表和权重转化为文本  
aspects_text = " ".join([aspect for aspect, weight in aspects.items() for _ in range(weight)])  
  
# 创建WordCloud对象  
wordcloud = WordCloud(width=800, height=400, background_color='white').generate(aspects_text)  
  
# 显示云图  
plt.figure(figsize=(10, 5))  
plt.imshow(wordcloud, interpolation='bilinear')  
plt.axis("off")  
plt.show()
~~~