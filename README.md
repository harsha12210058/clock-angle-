# clock-angle-
#clock angle problem        python
import sys
def angle_clock(time):
    hour, minute = time.split(':')
    hour = int(hour)
    minute = int(minute)
    angle = abs(hour%12 * 30 + minute * 0.5 - minute * 6)
    return min(angle, 360 - angle)

time = sys.stdin.readline().strip()
print(angle_clock(time))
