
ifndef $(LCT_SVC_PRJ_ROOT)
ROOT_DIR_SUFFIX_PART := $(lastword  $(subst src, ,$(CURDIR)))
LCT_SVC_PRJ_ROOT     := $(firstword $(subst /src$(ROOT_DIR_SUFFIX_PART), ,$(CURDIR)))
endif

TARGET_TYPE       = app
SRC_SUFFIX        = cpp
INC_DIR           += -I$(LCT_SVC_PRJ_ROOT)/src/3rdparty/cassandra/include

SYS_LIB           += -pthread 

DEP_OBJ           += $(LCT_SVC_PRJ_ROOT)/src/3rdparty/cassandra/lib/libcassandra_static.a
DEP_OBJ           += $(LCT_SVC_PRJ_ROOT)/src/3rdparty/uv/lib/libuv.a

TARGET            := cassandra-native-client-usage-sample

include $(LCT_SVC_PRJ_ROOT)/src/common/common.mk

