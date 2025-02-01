from PyQt5 import QtCore, QtGui, QtWidgets


class Ui_MainWindow(object):
     def win(self):
        self.wrong1.hide()
        self.wrong2.hide()
        self.wrong3.hide()
        self.wrigh_answ.hide()
        self.label.hide()
        self.pushButton.hide()
        self.play_again.show()
        self.label_2.show()
        self.label_2.setText('WIN!')
    
     def lose(self):
        self.wrong1.hide()
        self.wrong2.hide()
        self.wrong3.hide()
        self.wrigh_answ.hide()
        self.label.hide()
        self.pushButton.hide()
        self.play_again.show()
        self.label_2.show()
        self.label_2.setText('LOSE')
    
     def check_result(self):
        answer = self.wrigh_answ.isChecked()
        index = False
        if answer:
            self.win()
            index = True
        elif index == False:
            self.lose()

     def again(self):
        self.wrong1.show()
        self.wrong2.show()
        self.wrong3.show()
        self.wrigh_answ.show()
        self.label.show()
        self.pushButton.show()
        self.label_2.hide()
        self.play_again.hide()

        self.main_btn.setExclusive(False)
        self.wrong1.setChecked(False)
        self.wrong2.setChecked(False)
        self.wrong3.setChecked(False)
        self.wrigh_answ.setChecked(False)
        self.main_btn.setExclusive(True)


     def setupUi(self, MainWindow):
        MainWindow.setObjectName("MainWindow")
        MainWindow.resize(800, 600)
        self.centralwidget = QtWidgets.QWidget(MainWindow)
        self.centralwidget.setObjectName("centralwidget")
        self.wrigh_answ = QtWidgets.QRadioButton(self.centralwidget)
        self.wrigh_answ.setGeometry(QtCore.QRect(180, 230, 91, 91))
        font = QtGui.QFont()
        font.setFamily("Arial")
        font.setPointSize(26)
        font.setBold(True)
        font.setWeight(75)
        self.wrigh_answ.setFont(font)
        self.wrigh_answ.setObjectName("wrigh_answ")
        self.main_btn = QtWidgets.QButtonGroup(MainWindow)
        self.main_btn.setObjectName("main_btn")
        self.main_btn.addButton(self.wrigh_answ)
        self.wrong1 = QtWidgets.QRadioButton(self.centralwidget)
        self.wrong1.setGeometry(QtCore.QRect(380, 230, 91, 91))
        font = QtGui.QFont()
        font.setFamily("Arial")
        font.setPointSize(26)
        font.setBold(True)
        font.setWeight(75)
        self.wrong1.setFont(font)
        self.wrong1.setObjectName("wrong1")
        self.main_btn.addButton(self.wrong1)
        self.wrong2 = QtWidgets.QRadioButton(self.centralwidget)
        self.wrong2.setGeometry(QtCore.QRect(170, 340, 91, 91))
        font = QtGui.QFont()
        font.setFamily("Arial")
        font.setPointSize(26)
        font.setBold(True)
        font.setWeight(75)
        self.wrong2.setFont(font)
        self.wrong2.setObjectName("wrong2")
        self.main_btn.addButton(self.wrong2)
        self.wrong3 = QtWidgets.QRadioButton(self.centralwidget)
        self.wrong3.setGeometry(QtCore.QRect(390, 340, 91, 91))
        font = QtGui.QFont()
        font.setFamily("Arial")
        font.setPointSize(26)
        font.setBold(True)
        font.setWeight(75)
        self.wrong3.setFont(font)
        self.wrong3.setObjectName("wrong3")
        self.main_btn.addButton(self.wrong3)
        self.pushButton = QtWidgets.QPushButton(self.centralwidget)
        self.pushButton.setGeometry(QtCore.QRect(230, 470, 201, 41))
        self.pushButton.setStyleSheet("QPushButton {\n"
"    background-color: gray; /* Обычный серый цвет */\n"
"    color: white; /* Белый текст */\n"
"    border: none; /* Без границ */\n"
"    padding: 10px 20px; /* Отступы внутри кнопки */\n"
"    font-size: 16px; /* Размер текста */\n"
"    border-radius: 20px; /* Закругленные углы */\n"
"}\n"
"\n"
"QPushButton:hover {\n"
"    background-color: darkgray; /* Темно-серый цвет при наведении */\n"
"}")
        self.pushButton.setObjectName("pushButton")
        self.label = QtWidgets.QLabel(self.centralwidget)
        self.label.setGeometry(QtCore.QRect(260, 110, 181, 111))
        font = QtGui.QFont()
        font.setFamily("Arial")
        font.setPointSize(24)
        font.setBold(True)
        font.setItalic(True)
        font.setWeight(75)
        self.label.setFont(font)
        self.label.setObjectName("label")
        self.label_2 = QtWidgets.QLabel(self.centralwidget)
        self.label_2.setGeometry(QtCore.QRect(230, 270, 211, 111))
        font = QtGui.QFont()
        font.setPointSize(20)
        font.setBold(True)
        font.setWeight(75)
        self.label_2.setFont(font)
        self.label_2.setText("")
        self.label_2.setObjectName("label_2")
        self.play_again = QtWidgets.QPushButton(self.centralwidget)
        self.play_again.setEnabled(True)
        self.play_again.setGeometry(QtCore.QRect(160, 460, 341, 51))
        self.play_again.setStyleSheet("QPushButton {\n"
"    background-color: gray; /* Обычный серый цвет */\n"
"    color: white; /* Белый текст */\n"
"    border: none; /* Без границ */\n"
"    padding: 10px 20px; /* Отступы внутри кнопки */\n"
"    font-size: 16px; /* Размер текста */\n"
"    border-radius: 20px; /* Закругленные углы */\n"
"}\n"
"\n"
"QPushButton:hover {\n"
"    background-color: darkgray; /* Темно-серый цвет при наведении */\n"
"}")
        self.play_again.setObjectName("play_again")
        MainWindow.setCentralWidget(self.centralwidget)
        self.menubar = QtWidgets.QMenuBar(MainWindow)
        self.menubar.setGeometry(QtCore.QRect(0, 0, 800, 26))
        self.menubar.setObjectName("menubar")
        MainWindow.setMenuBar(self.menubar)
        self.statusbar = QtWidgets.QStatusBar(MainWindow)
        self.statusbar.setObjectName("statusbar")
        MainWindow.setStatusBar(self.statusbar)

        self.retranslateUi(MainWindow)
        QtCore.QMetaObject.connectSlotsByName(MainWindow)
        self.play_again.hide()
        self.label_2.hide()
        self.pushButton.clicked.connect(self.check_result)
        self.play_again.clicked.connect(self.again)

     def retranslateUi(self, MainWindow):
        _translate = QtCore.QCoreApplication.translate
        MainWindow.setWindowTitle(_translate("MainWindow", "MainWindow"))
        self.wrigh_answ.setText(_translate("MainWindow", "46"))
        self.wrong1.setText(_translate("MainWindow", "47"))
        self.wrong2.setText(_translate("MainWindow", "24"))
        self.wrong3.setText(_translate("MainWindow", "78"))
        self.pushButton.setText(_translate("MainWindow", "Ответить"))
        self.label.setText(_translate("MainWindow", "23+23 ="))
        self.play_again.setText(_translate("MainWindow", "Играть снова"))
        
        


if __name__ == "__main__":
    import sys
    app = QtWidgets.QApplication(sys.argv)
    MainWindow = QtWidgets.QMainWindow()
    ui = Ui_MainWindow()
    ui.setupUi(MainWindow)
    MainWindow.show()
    sys.exit(app.exec_())
