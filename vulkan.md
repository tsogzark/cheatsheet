# 1

```
​Validation Error: [ VUID-VkSwapchainCreateInfoKHR-imageFormat-01778 ] Object 0: handle = 0x207570b31b0, type = VK_OBJECT_TYPE_DEVICE; | MessageID = 0xc036022f | vkCreateSwapchainKHR(): pCreateInfo->imageFormat VK_FORMAT_B8G8R8A8_SRGB with tiling VK_IMAGE_TILING_OPTIMAL has no supported format features on this physical device. The Vulkan spec states: The implied image creation parameters of the swapchain must be supported as reported by vkGetPhysicalDeviceImageFormatProperties (https://vulkan.lunarg.com/doc/view/1.3.204.1/windows/1.3-extensions/vkspec.html#VUID-VkSwapchainCreateInfoKHR-imageFormat-01778)
```
> - VK_VERSION_1_3 --> VK_API_VERSION_1_3

# 2

- 卡死在waitforfence
> - 未使用该fence
```
_graphicsQueue.submit(submit, _cmdAvaliable);
```

# 3

- 无验证层信息
> - 没有启用验证层
> - 同时开启验证与RENDERDOC层

# 4
- 等待一个无法被signal的semaphore
> - 该semaphore未被进行signal调用