# SUSU_Timer
A useful timer in Linux. It can accurate to [ms] , the delta is 100-300 [us] in most Linux system. I always use it to something about performance optimization。

# HOW TO USE this timer


using namespace susu_tools;

int main()

{

    susu_timer time_tool;
	
    time_tool.begin();
	
    time_tool.delay(3,500);
	
    time_tool.end();
	
    timeval ret = time_tool.get_difference();
	
    printf("the time difference is %ld sec %ld ms %ld us\n",ret.tv_sec,ret.tv_usec/1000,ret.tv_usec%1000);
	
    return 0;
	
}