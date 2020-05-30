import pygame
import math
import time
pygame.init()

screen = pygame.display.set_mode([500, 500])
radius = 100
circumference = math.pi * radius
travel_speed = circumference/360
travelling = 0
position = (radius, 250)
angle = 0
running = True


def circle(travelling, x, y, new_position):
	pygame.draw.circle(screen, (0, 0, 255), (int(new_position[0]), position[1]), radius)
	pygame.draw.line(screen, (255, 0, 255), (new_position[0], position[1]), (x+travelling, y), 10)

while running:

    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False


    screen.fill((255, 255, 255))
    angle += 1
    x = position[0] + math.cos(math.radians(angle)) * radius
    y = position[1] + math.sin(math.radians(angle)) * radius

    
    pygame.draw.line(screen, (0, 0, 0), (0+radius, 250+radius), (0+radius+circumference, (250+radius)), 1)

    travelling += travel_speed
    new_position = [position[0]+travelling,position[1]+travelling]
    circle(travelling, x, y, new_position)

    if angle == 360:
    	angle = 0
    	travelling = 0

    pygame.display.flip()	
    time.sleep(0.01)


pygame.quit()
