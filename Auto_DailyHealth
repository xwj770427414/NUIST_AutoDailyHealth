"""
coding: UTF-8
Author: Wenjie Xu
Time: 2021/2/4 21:40
Environment: Python3.6
Email: xwj770427414@126.com
File: 自动填报.py
"""
from selenium import webdriver
from selenium.webdriver.support.wait import WebDriverWait
import time


# 登录网页

def login(id_stu, password):
    driver.find_element_by_id("username").click()  # 点击账号框
    driver.find_element_by_id("username").send_keys(id_stu)  # 输入账号
    driver.find_element_by_id("password").click()  # 点击密码框
    driver.find_element_by_id("password").send_keys(password)  # 输入密码
    driver.find_element_by_id("login_submit").click()  # 点击登陆
    time.sleep(5)


if __name__ == "__main__":
    # 实例化chrome浏览器对象
    driver = webdriver.Chrome()
    # 打开网站
    driver.get("http://my.nuist.edu.cn")
    # 设置十秒加载等待
    wait = WebDriverWait(driver, 10)
    # 设置登录账号和密码
    id = '***'
    password = '***'
    login(id, password)
    # 打开健康日报界面
    driver.get("http://e-office2.nuist.edu.cn/taskcenter/workflow/index")
    driver.get("http://e-office2.nuist.edu.cn/infoplus/form/XNYQSB/start")
    # 输入体温并确认
    driver.find_element_by_css_selector("input[name='fieldCNS']").click()
    driver.find_element_by_css_selector("input[name='fieldSTQKfrtw']").send_keys("36.1")
    driver.execute_script("$('nobr:contains(确认填报)').click()")
    time.sleep(5)
    driver.find_element_by_css_selector("button.dialog_button.default.fr").click()
    final = driver.find_element_by_css_selector("button.dialog_button.default.fr")
    final.click()
    # 关闭实例
    driver.quit()
