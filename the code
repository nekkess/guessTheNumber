from flask import Flask
import random
app = Flask(__name__)


def make_bold(function):
    def wrapper():
        return "<b>" + function() + "</b>"
    return wrapper

@app.route('/')
@make_bold
def guess_the_number():
    return '<h1>Guess a number between 0 and 9</h1>' \
           '<img src="https://media.giphy.com/media/3o7aCSPqXE5C6T8tBC/giphy.gif">'

@app.route('/<int:number>')
def check_the_choice(number):
    rnum = random.randint(0, 9)
    if number == rnum:
        return '<h1>Correct!!!You win nothing!!!</h1>' \
               '<img src="https://media2.giphy.com/media/iE4e5c8ExJUhdhvSiw/giphy.gif?cid=ecf05e479zjz2qtopuznye039wciwf39yjktufjo680didss&rid=giphy.gif&ct=g">'
    elif number > rnum:
        return '<h1>Too high!!!Retard!!!</h1>' \
               '<img src="https://media1.giphy.com/media/QObPo575HQHlGMhbae/giphy.gif?cid=ecf05e47jo23lgegqle6gj18pcbgronag391fv3pgw1orrtz&rid=giphy.gif&ct=g">'
    else:
        return '<h1>Too low!!!Brain damage detected!!!</h1>' \
               '<img src="https://media1.giphy.com/media/VUcIBmqLJ0DE3C9ue3/giphy.gif?cid=ecf05e47ooaiu2xutef28wecnmm2fdo6yz9wraiom8ckrory&rid=giphy.gif&ct=g">'


if __name__ == '__main__':
    app.run(debug=True)
