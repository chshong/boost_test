# Webots Makefile system
#
# You may add some variable definitions hereafter to customize the build process
# See documentation in $(WEBOTS_HOME_PATH)/resources/Makefile.include

# Should be CXXFLAGS, but webots uses CFLAGS for both of C and C++
CFLAGS = -Wall -Wextra -std=c++14 -pedantic -O2 -D__USE_W32_SOCKETS -D_WIN32_WINNT=0x501 -DWIN32
LFLAGS = 

# Do not modify the following: this includes Webots global Makefile.include
space :=
space +=
WEBOTS_HOME_PATH=$(subst $(space),\ ,$(strip $(subst \,/,$(WEBOTS_HOME))))
include $(WEBOTS_HOME_PATH)/resources/Makefile.include

INCLUDE += -I ../../boost/include
LIBRARIES += -L ../../boost/lib

# winsock
LIBRARIES += -lws2_32 -lwsock32
BOOST_POSTFIX = -mt

LIBRARIES += -lboost_system$(BOOST_POSTFIX)
