# euclidean-distance-calculator
#this code takes coordinates and calculates the distance between them
coordinate=[(3,7),(4,10),(6,12)]
lenght=len(coordinate)
distances = [0] * (lenght * (lenght - 1) // 2)
j=0
print("x1:",coordinate[0][0],"y1:",coordinate[0][1])
print("x2:",coordinate[1][0],"y2:",coordinate[1][1])
print("x3:",coordinate[2][0],"y3:",coordinate[2][1])

def euclideanDistance(a,b):
  euclidean=0
  for x in range(2) :
    euclidean+=((a[x]-b[x])**2)
  return euclidean**(1/2)
    
for i in range(lenght):
   for j in range(i+1,lenght):
      distance=euclideanDistance(coordinate[i],coordinate[j])
      distance=int(distance)
      distances[i*(lenght-1)-i*(i+1)//2+j-1]=distance
      


print(distances)
min_distance=min(distances)

print("min distance is:",min_distance)
