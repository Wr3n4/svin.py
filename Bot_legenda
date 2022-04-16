class Robot:
    def __init__(self):
        self.x, self.y, self.steps = 0, 0, 0
        self.pos = 'u'
        self.a = []

    def board(self, x, y):
        self.a = [[0 for _ in range(x)] for _ in range(y)]
        self.x, self.y = x // 2 + 1, y // 2 + 1

    def move(self):
        if self.pos == 'u':
            if self.a[self.x][self.y + 1] == 1:
                return
            else:
                self.y += 1
                self.a[self.x][self.y] = 1
        elif self.pos == 'd':
            if self.a[self.x][self.y - 1] == 1:
                return
            else:
                self.y -= 1
                self.a[self.x][self.y] = 1
        elif self.pos == 'r':
            if self.a[self.x + 1][self.y] == 1:
                return
            else:
                self.x += 1
                self.a[self.x][self.y] = 1
        elif self.pos == 'l':
            if self.a[self.x - 1][self.y] == 1:
                return
            else:
                self.x -= 1
                self.a[self.x][self.y] = 1
        self.steps += 1

    def rotate(self, cor):
        if cor == 'Right' or cor == 'R':
            if self.pos == 'u':
                self.pos = 'r'
            elif self.pos == 'r':
                self.pos = 'd'
            elif self.pos == 'd':
                self.pos = 'l'
            elif self.pos == 'l':
                self.pos = 'u'

        elif cor == 'Left' or cor == 'L':

            if self.pos == 'u':
                self.pos = 'l'
            elif self.pos == 'r':
                self.pos = 'u'
            elif self.pos == 'd':
                self.pos = 'r'
            elif self.pos == 'l':
                self.pos = 'd'

    def __str__(self):
        return f'X: {self.x}\tY: {self.y}'

    def board_info(self):
        return self.a


robot = Robot()
robot.board(102, 102)
robot.rotate('R')
robot.move()
robot.rotate('L')
robot.move()
for line in robot.board_info():
    print(line)
    
