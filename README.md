# Json-to-xml-conversion


import sys
import json
import xmltodict
inputFile = sys.argv[1]
outputFile = sys.argv[2]


with open(inputFile, 'r') as xml_file:
    myJson = xmltodict.parse(xml_file.read())

xml_file.close()

json_data = json.dumps(myJson)

#withfie opening command for json 
with open('output.json', 'w') as json_file:
    json_file.write(json_data)
