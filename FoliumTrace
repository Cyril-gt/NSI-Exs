import folium
f = open("Trace.csv", "r")
entete = f.readline()
line = f.readline()
cos=line.split(";")
carte=folium.Map(location=[float(cos[0]), float(cos[1])], zoom_start=14)
while line != "":
    lat,lon = line.split(";")
    folium.Circle([float(lat),float(lon)], radius=1).add_to(carte)
    line = f.readline()
f.close()
carte.save("trace.html")
