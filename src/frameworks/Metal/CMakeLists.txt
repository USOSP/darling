project(Metal)

remove_sdk_framework(Metal)

set(DYLIB_COMPAT_VERSION "1.0.0")
set(DYLIB_CURRENT_VERSION "1.0.0")

file(GLOB MTL_C src/*.c)
file(GLOB MTL_OBJC src/*.m)

set(FRAMEWORK_VERSION "A")

generate_sdk_framework(Metal
    VERSION ${FRAMEWORK_VERSION}
    HEADER "include/Metal"
)

add_framework(Metal
	FAT
	CURRENT_VERSION
	VERSION ${FRAMEWORK_VERSION}

	SOURCES
		src/_MTLCommandBuffer.m
		src/_MTLCommandEncoder.m
		src/_MTLCommandQueue.m
		src/_MTLComputePipelineState.m
		src/_MTLDebugCommandEncoder.m
		src/_MTLDepthStencilState.m
		src/_MTLDevice.m
		src/_MTLFakeComputePipelineState.m
		src/_MTLFunctionInternal.m
		src/_MTLFunction.m
		src/_MTLLibrary.m
		src/_MTLParallelRenderCommandEncoder.m
		src/_MTLRenderPipelineState.m
		src/_MTLSamplerState.m
		src/functions.c
		src/MTLArgumentInternal.m
		src/MTLArgument.m
		src/MTLArrayTypeInternal.m
		src/MTLArrayType.m
		src/MTLAttributeDescriptorArrayInternal.m
		src/MTLAttributeDescriptorArray.m
		src/MTLAttributeDescriptorInternal.m
		src/MTLAttributeDescriptor.m
		src/MTLAttributeInternal.m
		src/MTLAttribute.m
		src/MTLBufferArgument.m
		src/MTLBufferLayoutDescriptorArrayInternal.m
		src/MTLBufferLayoutDescriptorArray.m
		src/MTLBufferLayoutDescriptorInternal.m
		src/MTLBufferLayoutDescriptor.m
		src/MTLBuiltInArgument.m
		src/MTLCommandQueueDescriptorInternal.m
		src/MTLCommandQueueDescriptor.m
		src/MTLCompileOptionsInternal.m
		src/MTLCompileOptions.m
		src/MTLCompiler.m
		src/MTLComputePipelineDescriptorInternal.m
		src/MTLComputePipelineDescriptor.m
		src/MTLComputePipelineReflectionInternal.m
		src/MTLComputePipelineReflection.m
		src/MTLDepthStencilDescriptorInternal.m
		src/MTLDepthStencilDescriptor.m
		src/MTLFunctionConstantInternal.m
		src/MTLFunctionConstant.m
		src/MTLFunctionConstantValuesInternal.m
		src/MTLFunctionConstantValues.m
		src/MTLFunctionVariant.m
		src/MTLIndexedConstantValue.m
		src/MTLIOAccelBlitCommandEncoder.m
		src/MTLIOAccelBuffer.m
		src/MTLIOAccelCommandBuffer.m
		src/MTLIOAccelCommandEncoder.m
		src/MTLIOAccelCommandQueue.m
		src/MTLIOAccelComputeCommandEncoder.m
		src/MTLIOAccelDebugCommandEncoder.m
		src/MTLIOAccelDevice.m
		src/MTLIOAccelDeviceShmem.m
		src/MTLIOAccelDeviceShmemPool.m
		src/MTLIOAccelParallelRenderCommandEncoder.m
		src/MTLIOAccelPooledResource.m
		src/MTLIOAccelRenderCommandEncoder.m
		src/MTLIOAccelResourceAllocation.m
		src/MTLIOAccelResource.m
		src/MTLIOAccelResourcePool.m
		src/MTLIOAccelTexture.m
		src/MTLIOMemoryInfo.m
		src/MTLNamedConstantValue.m
		src/MTLPixelFormatQuery.m
		src/MTLRenderPassAttachmentDescriptor.m
		src/MTLRenderPassColorAttachmentDescriptorArrayInternal.m
		src/MTLRenderPassColorAttachmentDescriptorArray.m
		src/MTLRenderPassColorAttachmentDescriptorInternal.m
		src/MTLRenderPassColorAttachmentDescriptor.m
		src/MTLRenderPassDepthAttachmentDescriptorInternal.m
		src/MTLRenderPassDepthAttachmentDescriptor.m
		src/MTLRenderPassDescriptorInternal.m
		src/MTLRenderPassDescriptor.m
		src/MTLRenderPassStencilAttachmentDescriptorInternal.m
		src/MTLRenderPassStencilAttachmentDescriptor.m
		src/MTLRenderPipelineColorAttachmentDescriptorArrayInternal.m
		src/MTLRenderPipelineColorAttachmentDescriptorArray.m
		src/MTLRenderPipelineColorAttachmentDescriptorInternal.m
		src/MTLRenderPipelineColorAttachmentDescriptor.m
		src/MTLRenderPipelineDescriptorInternal.m
		src/MTLRenderPipelineDescriptor.m
		src/MTLRenderPipelineReflectionInternal.m
		src/MTLRenderPipelineReflection.m
		src/MTLResourceAllocationInfo.m
		src/MTLResourceList.m
		src/MTLResourceListPool.m
		src/MTLSamplerDescriptorInternal.m
		src/MTLSamplerDescriptor.m
		src/MTLStageInputOutputDescriptorInternal.m
		src/MTLStageInputOutputDescriptor.m
		src/MTLStencilDescriptorInternal.m
		src/MTLStencilDescriptor.m
		src/MTLStructMemberInternal.m
		src/MTLStructMember.m
		src/MTLStructTypeInternal.m
		src/MTLStructType.m
		src/MTLTextureArgument.m
		src/MTLTextureDescriptorInternal.m
		src/MTLTextureDescriptor.m
		src/MTLThreadgroupMemoryArgument.m
		src/MTLVertexAttributeDescriptorArrayInternal.m
		src/MTLVertexAttributeDescriptorArray.m
		src/MTLVertexAttributeDescriptorInternal.m
		src/MTLVertexAttributeDescriptor.m
		src/MTLVertexAttributeInternal.m
		src/MTLVertexAttribute.m
		src/MTLVertexBufferLayoutDescriptorArrayInternal.m
		src/MTLVertexBufferLayoutDescriptorArray.m
		src/MTLVertexBufferLayoutDescriptorInternal.m
		src/MTLVertexBufferLayoutDescriptor.m
		src/MTLVertexDescriptorInternal.m
		src/MTLVertexDescriptor.m

	DEPENDENCIES
		system
		objc
		Foundation
)
