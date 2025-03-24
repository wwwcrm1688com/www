接下来，我们定义一个Track类，表示赛道。为了简单起见，我们将赛道定义为一条直线，并添加边界检测
class Track:
    def __init__(self, start_x, end_x, y, width):
        self.start_x = start_x
        self.end_x = end_x
        self.y = y
        self.width = width

    def is_in_track(self, kart):
        return (self.start_x <= kart.x <= self.end_x) and (self.y - self.width <= kart.y <= self.y + self.width)

    def __str__(self):
        return f"Track(start_x={self.start_x}, end_x={self.end_x}, y={self.y}, width={self.width})"
