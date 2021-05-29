################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F7xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
BSL_1_System.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
BSL_1_System.list \

OBJCOPY_BIN += \
BSL_1_System.bin \


# All Target
all: BSL_1_System.elf secondary-outputs

# Tool invocations
BSL_1_System.elf: $(OBJS) $(USER_OBJS) C:\Users\arturo\STM32CubeIDE\workspace2\BSL_1_System\STM32F767ZITX_FLASH.ld
	arm-none-eabi-gcc -o "BSL_1_System.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m7 -T"C:\Users\arturo\STM32CubeIDE\workspace2\BSL_1_System\STM32F767ZITX_FLASH.ld" --specs=nosys.specs -Wl,-Map="BSL_1_System.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv5-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

BSL_1_System.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "BSL_1_System.list"
	@echo 'Finished building: $@'
	@echo ' '

BSL_1_System.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "BSL_1_System.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
