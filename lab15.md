智能蛇学习

a  构造一条蛇
所用知识：应用二维数组，并初始化，标明蛇头与蛇尾。
蛇脑袋的值是最大的,蛇尾是最小的, 这样写得目的是为了, 
蛇移动时, 只需要移动蛇脑袋和蛇尾部即可, 蛇尾部移动规律
就是找到比它大一的那个值.所以设置为int类型.

void CreateSnake(int snake[ROW_MAX][LINE_MAX]){

    int i, j;
    int value = Head_v;
    snake[Head_x][Head_y] = value;

    for(i = Head_x, j = Head_y+1; j < Head_y + de_lenth; ++j)
        snake[i][j] = --value;
    Tail_x = i;
    Tail_y = --j;
}

b  产生食物
   所用知识：二维数组。
   要求，
   食物不能与墙以及蛇身体重合. 
   食物放到地图的数组里.
   void CreateFood(char map[ROW_MAX][LINE_MAX], int snake[ROW_MAX][LINE_MAX]){

    int food_x = 0;
    int food_y = 0;

    while (map[food_x][food_y] == '#' || snake[food_x][food_y] != 0){

        food_x = rand()%(ROW_MAX-3) + 1;
        food_y = rand()%(LINE_MAX-3) + 1;
    }

    map[food_x][food_y] = 'O';
}
c 判断是否撞墙，若撞墙，则游戏终止。
nt JudgeWall(void){

    if((Head_x == 0 || Head_x == ROW_MAX-1) || (Head_y == 0 || Head_y == LINE_MAX-1))
        return 0;
    else 
        return 1;
}

d  蛇如何吃到食物

   int EatFood(char map[ROW_MAX][LINE_MAX]){

    if(map[Head_x][Head_y] == 'O'){

        map[Head_x][Head_y] = 0;
        count++;
        return 0;
    }
    else
        return 1;
}
e  蛇如何运动；
   这部分太过复杂，没有理解。
   