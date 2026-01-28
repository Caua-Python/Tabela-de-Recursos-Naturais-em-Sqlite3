# Tabela-de-Recursos-Naturais-em-Sqlite3

import sqlite3

conn = sqlite3.connect("natural_resources.db")

cursor = conn.cursor()


def create():

    sql = """

    CREATE TABLE albums(product text, register text, price text, enterprise text)

    """

    cursor.execute(sql)

    conn.commit()

def insert():

    sql = "INSERT INTO albums VALUES('Iron', '015942', '$90,00 USD', 'JacquesSELL Group')"

    cursor.execute(sql)

    conn.commit()

def other():

    a1 = input('Write one resource: ')
    a2 = int(input('Write one register: '))
    a3 = f"$ {float(input('Write the price: ')):.2f} USD"
    a4  = input('Write the namer of the enterprise: ')

    b1 = input('Write one resource: ')
    b2 = int(input('Write one register: '))
    b3 = f"$ {float(input('Write the price: ')):.2f} USD"
    b4 = input('Write the namer of the enterprise: ')

    c1 = input('Write one resource: ')
    c2 = int(input('Write one register: '))
    c3 = f"$ {float(input('Write the price: ')):.2f} USD"
    c4  = input('Write the namer of the enterprise: ')

    d1 = input('Write one resource: ')
    d2 = int(input('Write one register: '))
    d3 = f"$ {float(input('Write the price: ')):.2f} USD"
    d4  = input('Write the namer of the enterprise: ')

    e1 = input('Write one resource: ')
    e2 = int(input('Write one register: '))
    e3 = f"$ {float(input('Write the price: ')):.2f} USD"
    e4 = input('Write the namer of the enterprise: ')




    albums = [(a1, a2, a3, a4), (b1, b2, b3, b4), (c1, c2, c3, c4), (d1, d2, d3, d4), (e1, e2, e3, e4)]

    cursor.executemany("INSERT INTO albums VALUES(?, ?, ?, ?)", albums)

    conn.commit()
