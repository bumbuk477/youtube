# youtube
from PyQt5.QtCore import *
from PyQt5.QtWidgets import *
def winner():
    window = QMessageBox
    window.setText("Правильно! Ви виграли гіроскутер")
    window.exec()
def looser():
    window = QMessageBox
    window.setText("Ні, в 2015 році. Ви виграли фірмовий плакат")
    window.exec()
app = QApplication([])
win = QWidget()
win.setWindowTitle("Конкурс від Crazy People")
win.resize(400,200)
win.move(100,100)
text = QLabel("В якому році канал отримав 'золоту кнопку'від YouTube?")
rbtn1 = QRadioButton("2005")
rbtn2 = QRadioButton("2010")
rbtn3 = QRadioButton("2015")
rbtn4 = QRadioButton("2020")
line= QVBoxLayout
line.addWidget(text,alignment=Qt.AlignCenter)
line1 = QHBoxLayout
line1.addWidget(rbtn1,alignment = Qt.AlignCenter)
line1.addWidget(rbtn2,alignment = Qt.AlignCenter)
line2= QHBoxLayout
line2.addWidget(rbtn3,alignment = Qt.AlignCenter)
line2.addWidget(rbtn4,alignment = Qt.AlignCenter)


line.addLayout(line1)
line.addLayout(line2)
rbtn3.clicked.connect(winner)
rbtn1.clicked.connect(looser)
rbtn2.clicked.connect(looser)
rbtn4.clicked.connect(looser)


win.show()
app.exec()
