# openssl-prebuilt

*OpenSSL v1.0.2l*

## Usage

```
LOCAL_PATH:= $(call my-dir)

include $(CLEAR_VARS)
LOCAL_MODULE := libcrypto
LOCAL_SRC_FILES := $(TARGET_ARCH_ABI)/libcrypto.a
include $(PREBUILT_STATIC_LIBRARY)

include $(CLEAR_VARS)
LOCAL_MODULE := libssl
LOCAL_SRC_FILES := $(TARGET_ARCH_ABI)/libssl.a
include $(PREBUILT_STATIC_LIBRARY)

include $(CLEAR_VARS)
LOCAL_MODULE := {Lib Name}
LOCAL_SRC_FILES := {Lib Src}
LOCAL_C_INCLUDES := \
	{include/openssl folder locatin}
LOCAL_SHARED_LIBRARIES := libcrypto libssl
LOCAL_LDLIBS := -lz -llog
include $(BUILD_SHARED_LIBRARY)
```
