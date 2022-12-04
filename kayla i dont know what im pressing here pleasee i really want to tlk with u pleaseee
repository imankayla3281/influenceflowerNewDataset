import os
import numpy as np
import json

id_list = []

def txt_to_json(filename):
    with open(filename + ".txt") as f1:
        cNames = f1.readlines()
        for i in range(0,len(cNames)-1):
            cNames[i] = cNames[i].strip()+','+'\n'
        cNames[0] = "[" + cNames[0]
        cNames[len(cNames)-1] = cNames[len(cNames)-1] + ']'

    with open(filename + ".txt", 'w') as f2:
        f2.writelines(cNames)

    os.rename(filename + ".txt",filename + ".json")

def getID(filename):
    f = open(filename + '.json')
    data = json.load(f)
    for i in data:
        id_list.append(i['sha'])

    print(id_list)

    f.close()
    
def saveID():
    with open("all-paper-ids.txt", "w") as output:
        output.write(str(id_list))

txt_to_json("one")
getID("one")

txt_to_json("two")
getID("two")

txt_to_json("three")
getID("three")

txt_to_json("four")
getID("four")

txt_to_json("five")
getID("five")

txt_to_json("six")
getID("six")

txt_to_json("seven")
getID("seven")

saveID()
