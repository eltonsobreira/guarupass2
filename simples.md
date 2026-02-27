import pandas
import pyautogui
import time
tabela = pandas.read_csv("Pasta1.csv", sep = ";")
print(tabela)

pyautogui.PAUSE = 1
pyautogui.hotkey("alt","tab")

for linha in tabela.index:
    pyautogui.hotkey("alt","I")
    pyautogui.press("enter")
    time.sleep(5)
    pyautogui.press("down")
    pyautogui.press("tab")   
    COD_IOB = tabela.loc[linha ,"COD_IOB"]
    pyautogui.write(str(COD_IOB))
    pyautogui.press("tab")
    pyautogui.press("enter")
    pyautogui.press("enter")

    EMISSAO = tabela.loc[linha , "EMISSAO"]
    pyautogui.write(str(EMISSAO))
    pyautogui.press("enter")

    VENCIMENTO = tabela.loc[linha , "VENCIMENTO"]
    pyautogui.write(str(VENCIMENTO))
    pyautogui.press("enter")
    pyautogui.press("enter")
    pyautogui.press("enter")
    pyautogui.press("enter")
    pyautogui.press("enter")
    pyautogui.press("enter")
    pyautogui.press("enter")
    pyautogui.press("enter")
    pyautogui.press("enter")
    pyautogui.press("enter")
    pyautogui.press("tab")
    pyautogui.press("tab")
    pyautogui.press("tab")
    pyautogui.press("tab")
    pyautogui.press("insert")
    pyautogui.write(str("C01"))
    pyautogui.press("tab")
    pyautogui.press("tab")
    pyautogui.press("tab")
    pyautogui.press("tab")
    pyautogui.press("tab")
    pyautogui.press("tab")
    pyautogui.write("1")
    pyautogui.press("tab")

    TOTAL = tabela.loc[linha , "TOTAL"]
    pyautogui.write(str(TOTAL))
    pyautogui.press("enter")
    pyautogui.press("esc")
    pyautogui.press("enter")
    time.sleep(2)
    pyautogui.hotkey("alt", "G")
    time.sleep(2)
    pyautogui.press("enter")
    pyautogui.press("enter")
    pyautogui.press("enter")
    pyautogui.press("enter")
    time.sleep(2)
