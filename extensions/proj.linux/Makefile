TARGET = libextension.a

COCOS_ROOT=../..

INCLUDES = -I$(COCOS_ROOT)/external \
	-I$(COCOS_ROOT)/external/chipmunk/include/chipmunk \
	-I$(COCOS_ROOT)/CocosDenshion/include \
	-I.. \
	-I../CCBReader \
	-I../GUI/CCControlExtension \
	-I../GUI/CCEditBox \
	-I../network \
	-I../Components \
	-I../CCArmature

SOURCES = ../CCBReader/CCBFileLoader.cpp \
../CCBReader/CCMenuItemImageLoader.cpp \
../CCBReader/CCBReader.cpp \
../CCBReader/CCMenuItemLoader.cpp \
../CCBReader/CCControlButtonLoader.cpp \
../CCBReader/CCNodeLoader.cpp \
../CCBReader/CCControlLoader.cpp \
../CCBReader/CCNodeLoaderLibrary.cpp \
../CCBReader/CCLabelBMFontLoader.cpp \
../CCBReader/CCParticleSystemQuadLoader.cpp \
../CCBReader/CCLabelTTFLoader.cpp \
../CCBReader/CCScale9SpriteLoader.cpp \
../CCBReader/CCLayerColorLoader.cpp \
../CCBReader/CCScrollViewLoader.cpp \
../CCBReader/CCLayerGradientLoader.cpp \
../CCBReader/CCSpriteLoader.cpp \
../CCBReader/CCLayerLoader.cpp \
../CCBReader/CCBAnimationManager.cpp \
../CCBReader/CCBKeyframe.cpp \
../CCBReader/CCBSequence.cpp \
../CCBReader/CCBSequenceProperty.cpp \
../CCBReader/CCBValue.cpp \
../CCBReader/CCNode+CCBRelativePositioning.cpp \
../GUI/CCScrollView/CCScrollView.cpp \
../GUI/CCScrollView/CCSorting.cpp \
../GUI/CCScrollView/CCTableView.cpp \
../GUI/CCScrollView/CCTableViewCell.cpp \
../GUI/CCControlExtension/CCControlButton.cpp \
../GUI/CCControlExtension/CCControlColourPicker.cpp \
../GUI/CCControlExtension/CCControl.cpp \
../GUI/CCControlExtension/CCControlHuePicker.cpp \
../GUI/CCControlExtension/CCControlSaturationBrightnessPicker.cpp \
../GUI/CCControlExtension/CCControlSlider.cpp \
../GUI/CCControlExtension/CCControlSwitch.cpp \
../GUI/CCControlExtension/CCControlUtils.cpp \
../GUI/CCControlExtension/CCInvocation.cpp \
../GUI/CCControlExtension/CCScale9Sprite.cpp \
../GUI/CCControlExtension/CCControlPotentiometer.cpp \
../GUI/CCControlExtension/CCControlStepper.cpp \
../GUI/CCEditBox/CCEditBox.cpp \
../GUI/CCEditBox/CCEditBoxImplNone.cpp \
../network/HttpClient.cpp \
../physics_nodes/CCPhysicsDebugNode.cpp \
../physics_nodes/CCPhysicsSprite.cpp \
../spine/Animation.cpp \
../spine/AnimationState.cpp \
../spine/AnimationStateData.cpp \
../spine/Atlas.cpp \
../spine/AtlasAttachmentLoader.cpp \
../spine/Attachment.cpp \
../spine/AttachmentLoader.cpp \
../spine/Bone.cpp \
../spine/BoneData.cpp \
../spine/Json.cpp \
../spine/RegionAttachment.cpp \
../spine/Skeleton.cpp \
../spine/SkeletonData.cpp \
../spine/SkeletonJson.cpp \
../spine/Skin.cpp \
../spine/Slot.cpp \
../spine/SlotData.cpp \
../spine/extension.cpp \
../spine/spine-cocos2dx.cpp \
../spine/CCSkeleton.cpp \
../spine/CCSkeletonAnimation.cpp \
../CCArmature/CCArmature.cpp \
../CCArmature/CCBone.cpp \
../CCArmature/animation/CCArmatureAnimation.cpp \
../CCArmature/animation/CCProcessBase.cpp \
../CCArmature/animation/CCTween.cpp \
../CCArmature/datas/CCDatas.cpp \
../CCArmature/display/CCBatchNode.cpp \
../CCArmature/display/CCDecorativeDisplay.cpp \
../CCArmature/display/CCDisplayFactory.cpp \
../CCArmature/display/CCDisplayManager.cpp \
../CCArmature/display/CCShaderNode.cpp \
../CCArmature/display/CCSkin.cpp \
../CCArmature/external_tool/GLES-Render.cpp \
../CCArmature/external_tool/Json/CSContentJsonDictionary.cpp \
../CCArmature/external_tool/Json/lib_json/json_value.cpp \
../CCArmature/external_tool/Json/lib_json/json_reader.cpp \
../CCArmature/external_tool/Json/lib_json/json_writer.cpp \
../CCArmature/physics/CCColliderDetector.cpp \
../CCArmature/physics/CCPhysicsWorld.cpp \
../CCArmature/utils/CCArmatureDataManager.cpp \
../CCArmature/utils/CCDataReaderHelper.cpp \
../CCArmature/utils/CCSpriteFrameCacheHelper.cpp \
../CCArmature/utils/CCTransformHelp.cpp \
../CCArmature/utils/CCTweenFunction.cpp \
../CCArmature/utils/CCUtilMath.cpp \
../Components/CCComAttribute.cpp \
../Components/CCComAudio.cpp \
../Components/CCComController.cpp \
../Components/CCInputDelegate.cpp \
../CCDeprecated-ext.cpp

include $(COCOS_ROOT)/cocos2dx/proj.linux/cocos2dx.mk

CXXFLAGS += -Wno-multichar

TARGET := $(LIB_DIR)/$(TARGET)

all: $(TARGET)

$(TARGET): $(OBJECTS) $(CORE_MAKEFILE_LIST)
	@mkdir -p $(@D)
	$(LOG_AR)$(AR) $(ARFLAGS) $@ $(OBJECTS)

$(OBJ_DIR)/%.o: ../%.cpp $(CORE_MAKEFILE_LIST)
	@mkdir -p $(@D)
	$(LOG_CXX)$(CXX) $(CXXFLAGS) $(INCLUDES) $(DEFINES) -c $< -o $@

$(OBJ_DIR)/%.o: ../%.c $(CORE_MAKEFILE_LIST)
	@mkdir -p $(@D)
	$(LOG_CC)$(CC) $(CCFLAGS) $(INCLUDES) $(DEFINES) -c $< -o $@
