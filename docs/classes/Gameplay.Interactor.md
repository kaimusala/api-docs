[Gameplay](../groups/Gameplay.Gameplay.md) / Interactor

# Interactor <Badge type="tip" text="Class" /> <Score text="Interactor" />

交互物功能对象 V2

## Hierarchy

- [`GameObject`](Gameplay.GameObject.md)

  ↳ **`Interactor`**

  ↳↳ [`InteractiveObject`](Gameplay.InteractiveObject.md)

## Table of contents

| Properties |
| :-----|
| **[onInteractiveEnded](Gameplay.Interactor.md#oninteractiveended)**: [`MulticastDelegate`](Type.MulticastDelegate.md)<() => `void`\> <br> 交互结束时执行绑定函数|
| **[onInteractiveStarted](Gameplay.Interactor.md#oninteractivestarted)**: [`MulticastDelegate`](Type.MulticastDelegate.md)<() => `void`\> <br> 交互开始时执行绑定函数|
| **[onInteractorEnter](Gameplay.Interactor.md#oninteractorenter)**: [`Delegate`](Type.Delegate.md)<(`result`: `boolean`) => `void`\> <br> （请不要使用此委托，绑定的回调会在调用交互时被重置，外部回调不会触发）激活交互时执行绑定函数|
| **[onInteractorExit](Gameplay.Interactor.md#oninteractorexit)**: [`Delegate`](Type.Delegate.md)<(`result`: `boolean`) => `void`\> <br> （请不要使用此委托，绑定的回调会在调用退出交互时被重置，外部回调不会触发）退出交互时执行绑定函数|

| Accessors |
| :-----|
| **[interactiveSlot](Gameplay.Interactor.md#interactiveslot)**(): [`InteractiveSlot`](../enums/Gameplay.InteractiveSlot.md) <br> 交互物插槽|
| **[interactiveStance](Gameplay.Interactor.md#interactivestance)**(): `string` <br> 交互动画姿态资源 id|


::: details 点击查看继承
| Accessors |
| :-----|
| **[forwardVector](Gameplay.GameObject.md#forwardvector)**(): [`Vector`](Type.Vector.md) <br> 获取当前物体的向前向量|
| **[guid](Gameplay.GameObject.md#guid)**(): `string` <br> 获取对象的GUID（唯一标识一个对象的字符串）。|
| **[lockStatus](Gameplay.GameObject.md#lockstatus)**(): `boolean` <br> 获取对象是否锁定|
| **[name](Gameplay.GameObject.md#name)**(): `string` <br> 返回当前物体名称|
| **[netStatus](Gameplay.GameObject.md#netstatus)**(): [`NetStatus`](../enums/Type.NetStatus.md) <br> 获取当前物体同步状态|
| **[parent](Gameplay.GameObject.md#parent)**(): `GameObject` <br> 获取当前父物体|
| **[relativeLocation](Gameplay.GameObject.md#relativelocation)**(): [`Vector`](Type.Vector.md) <br> 获取相对位置|
| **[relativeRotation](Gameplay.GameObject.md#relativerotation)**(): [`Rotation`](Type.Rotation.md) <br> 获取相对旋转|
| **[relativeScale](Gameplay.GameObject.md#relativescale)**(): [`Vector`](Type.Vector.md) <br> 获取相对缩放|
| **[rightVector](Gameplay.GameObject.md#rightvector)**(): [`Vector`](Type.Vector.md) <br> 获取当前物体的向右向量|
| **[staticStatus](Gameplay.GameObject.md#staticstatus)**(): `boolean` <br> 获取对象是否静态|
| **[tag](Gameplay.GameObject.md#tag)**(): `string` <br> 获取当前物体的Tag|
| **[transform](Gameplay.GameObject.md#transform)**(): [`Transform`](Type.Transform.md) <br> 返回当前物体transform|
| **[upVector](Gameplay.GameObject.md#upvector)**(): [`Vector`](Type.Vector.md) <br> 获取当前物体的向上向量|
| **[useUpdate](Gameplay.GameObject.md#useupdate)**(): `boolean` <br> 获取对象是否使用更新|
| **[visible](Gameplay.GameObject.md#visible)**(): `boolean` <br> 获取当前物体是否显示|
| **[worldLocation](Gameplay.GameObject.md#worldlocation)**(): [`Vector`](Type.Vector.md) <br> 获取物体的世界坐标|
| **[worldRotation](Gameplay.GameObject.md#worldrotation)**(): [`Rotation`](Type.Rotation.md) <br> 获取物体的世界旋转|
| **[worldScale](Gameplay.GameObject.md#worldscale)**(): [`Vector`](Type.Vector.md) <br> 获取物体的世界缩放|
:::


| Methods |
| :-----|
| **[endInteract](Gameplay.Interactor.md#endinteract)**(`endLoc?`: [`Vector`](Type.Vector.md), `endRot?`: [`Rotation`](Type.Rotation.md), `newStance?`: `string`): `boolean` <br> 结束交互|
| **[enterInteractiveState](Gameplay.Interactor.md#enterinteractivestate)**(`characterObj`: `GameObject`): `Promise`<`boolean`\> <br> 激活交互，将角色切换到特定姿态和位置，并绑定到交互物上|
| **[exitInteractiveState](Gameplay.Interactor.md#exitinteractivestate)**(`Location`: [`Vector`](Type.Vector.md), `stance?`: `string`): `Promise`<`boolean`\> <br> 退出交互，恢复角色的绑定关系，姿态和位置|
| **[getInteractCharacter](Gameplay.Interactor.md#getinteractcharacter)**(): [`CharacterBase`](Gameplay.CharacterBase.md) <br> 获取正在交互的角色|
| **[getInteractiveState](Gameplay.Interactor.md#getinteractivestate)**(): `boolean` <br> 获取该交互物的交互状态|
| **[getInteractiveStatus](Gameplay.Interactor.md#getinteractivestatus)**(): `boolean` <br> 获取该交互物的交互状态|
| **[interactiveCharacter](Gameplay.Interactor.md#interactivecharacter)**(): [`Character`](Gameplay.Character.md) <br> 获取和交互物发生交互的角色|
| **[startInteract](Gameplay.Interactor.md#startinteract)**(`newCharObj`: [`CharacterBase`](Gameplay.CharacterBase.md), `newSlot?`: [`InteractiveSlot`](../enums/Gameplay.InteractiveSlot.md), `newStance?`: `string`): `boolean` <br> 开始交互|


::: details 点击查看继承
| Methods |
| :-----|
| **[addDestroyCallback](Gameplay.GameObject.md#adddestroycallback)**(`callback`: (...`arg`: `unknown`[]) => `void`): `void` <br> 添加物体Destroy事件回调|
| **[asyncGetScriptByName](Gameplay.GameObject.md#asyncgetscriptbyname)**(`name`: `string`): `Promise`<`Script`\> <br> 异步获得当前物体下的指定脚本 客户端不维系父子关系|
| **[attachComponent](Gameplay.GameObject.md#attachcomponent)**(`component`: `Component`, `isStatic?`: `boolean`): `boolean` <br> 附加组件|
| **[attachToGameObject](Gameplay.GameObject.md#attachtogameobject)**(`obj`: `GameObject`): `void` <br> 将物体附着到指定物体上|
| **[clone](Gameplay.GameObject.md#clone)**(`spawnInfo?`: `boolean` \): `GameObject` <br> 复制对象|
| **[deleteDestroyCallback](Gameplay.GameObject.md#deletedestroycallback)**(`callback`: (...`arg`: `unknown`[]) => `void`): `void` <br> 移除物体Destroy事件回调|
| **[destroy](Gameplay.GameObject.md#destroy)**(): `void` <br> 删除对象|
| **[detachComponent](Gameplay.GameObject.md#detachcomponent)**(`component`: `string` \): `void` <br> 移除组件|
| **[detachFromGameObject](Gameplay.GameObject.md#detachfromgameobject)**(): `void` <br> 将此物体与当前附着的物体分离|
| **[getBoundingBoxSize](Gameplay.GameObject.md#getboundingboxsize)**(`nonColliding?`: `boolean`, `includeFromChildActors?`: `boolean`, `outer?`: [`Vector`](Type.Vector.md)): [`Vector`](Type.Vector.md) <br> 获取物体包围盒大小|
| **[getBounds](Gameplay.GameObject.md#getbounds)**(`onlyCollidingComponents`: `boolean`, `OriginOuter`: [`Vector`](Type.Vector.md), `BoxExtentOuter`: [`Vector`](Type.Vector.md), `includeFromChildActors?`: `boolean`): `void` <br> 获取GameObject边界|
| **[getChildByGuid](Gameplay.GameObject.md#getchildbyguid)**(`GUID`: `string`): `undefined` \| `GameObject` <br> 根据GUID查找子物体|
| **[getChildByName](Gameplay.GameObject.md#getchildbyname)**(`name`: `string`): `undefined` \| `GameObject` <br> 根据名称查找子物体|
| **[getChildren](Gameplay.GameObject.md#getchildren)**(): `undefined` \| `GameObject`[] <br> 获取Children，客户端不维系父子关系。推荐使用Find替代|
| **[getChildrenBoxCenter](Gameplay.GameObject.md#getchildrenboxcenter)**(`outer?`: [`Vector`](Type.Vector.md)): [`Vector`](Type.Vector.md) <br> 获取所有子对象包围盒中心点(不包含父对象,父对象不可用返回[0,0,0])|
| **[getCollision](Gameplay.GameObject.md#getcollision)**(): [`PropertyStatus`](../enums/Type.PropertyStatus.md) \| [`CollisionStatus`](../enums/Type.CollisionStatus.md) <br> 返回碰撞状态|
| **[getForwardVector](Gameplay.GameObject.md#getforwardvector)**(`outer?`: [`Vector`](Type.Vector.md)): [`Vector`](Type.Vector.md) <br> 获取当前物体的向前向量|
| **[getRelativeLocation](Gameplay.GameObject.md#getrelativelocation)**(`outer?`: [`Vector`](Type.Vector.md)): [`Vector`](Type.Vector.md) <br> 获取相对位置|
| **[getRelativeRotation](Gameplay.GameObject.md#getrelativerotation)**(`outer?`: [`Rotation`](Type.Rotation.md)): [`Rotation`](Type.Rotation.md) <br> 获取相对旋转|
| **[getRelativeScale](Gameplay.GameObject.md#getrelativescale)**(`outer?`: [`Vector`](Type.Vector.md)): [`Vector`](Type.Vector.md) <br> 获取相对缩放|
| **[getRightVector](Gameplay.GameObject.md#getrightvector)**(`outer?`: [`Vector`](Type.Vector.md)): [`Vector`](Type.Vector.md) <br> 获取当前物体的向右向量|
| **[getScriptByGuid](Gameplay.GameObject.md#getscriptbyguid)**(`GUID`: `string`): `undefined` \| `Script` <br> 获得当前物体下的指定脚本|
| **[getScriptByName](Gameplay.GameObject.md#getscriptbyname)**(`name`: `string`): `undefined` \| `Script` <br> 获得当前物体下的指定脚本|
| **[getScripts](Gameplay.GameObject.md#getscripts)**(): `undefined` \| `Script`[] <br> 获得当前物体下的所有脚本|
| **[getSourceAssetGuid](Gameplay.GameObject.md#getsourceassetguid)**(): `string` <br> 获取当前物体使用资源的GUID|
| **[getTransform](Gameplay.GameObject.md#gettransform)**(`outer?`: [`Transform`](Type.Transform.md)): [`Transform`](Type.Transform.md) <br> 返回当前物体Transform|
| **[getUpVector](Gameplay.GameObject.md#getupvector)**(`outer?`: [`Vector`](Type.Vector.md)): [`Vector`](Type.Vector.md) <br> 获取当前物体的向上向量|
| **[getVisibility](Gameplay.GameObject.md#getvisibility)**(): `boolean` <br> 获取GameObject是否被显示|
| **[getWorldLocation](Gameplay.GameObject.md#getworldlocation)**(`outer?`: [`Vector`](Type.Vector.md)): [`Vector`](Type.Vector.md) <br> 获取物体的世界坐标|
| **[getWorldRotation](Gameplay.GameObject.md#getworldrotation)**(`outer?`: [`Rotation`](Type.Rotation.md)): [`Rotation`](Type.Rotation.md) <br> 获取物体的世界旋转|
| **[getWorldScale](Gameplay.GameObject.md#getworldscale)**(`outer?`: [`Vector`](Type.Vector.md)): [`Vector`](Type.Vector.md) <br> 获取物体的世界缩放|
| **[isRunningClient](Gameplay.GameObject.md#isrunningclient)**(): `boolean` <br> 是否为客户端|
| **[onDestroy](Gameplay.GameObject.md#ondestroy)**(): `void` <br> 周期函数 被销毁时调用|
| **[onReplicated](Gameplay.GameObject.md#onreplicated)**(`path`: `string`, `value`: `unknown`, `oldVal`: `unknown`): `void` <br> 属性被同步事件 ClientOnly|
| **[onStart](Gameplay.GameObject.md#onstart)**(): `void` <br> 周期函数 脚本开始执行时调用|
| **[onUpdate](Gameplay.GameObject.md#onupdate)**(`dt`: `number`): `void` <br> 周期函数 useUpdate 设置为 true 后,每帧被执行,设置为false,不会执行|
| **[ready](Gameplay.GameObject.md#ready)**(): `Promise`<[`GameObject`](Gameplay.GameObject.md)\> <br> GameObject准备好后返回|
| **[setCollision](Gameplay.GameObject.md#setcollision)**(`status`: [`PropertyStatus`](../enums/Type.PropertyStatus.md) \, `propagateToChildren?`: `boolean`): `void` <br> 设置碰撞状态|
| **[setLocationAndRotation](Gameplay.GameObject.md#setlocationandrotation)**(`location`: [`Vector`](Type.Vector.md), `rotation`: [`Rotation`](Type.Rotation.md)): `void` <br> 同时设置物体的世界位置与旋转|
| **[setRelativeLocation](Gameplay.GameObject.md#setrelativelocation)**(`location`: [`Vector`](Type.Vector.md)): `void` <br> 设置相对位置|
| **[setRelativeRotation](Gameplay.GameObject.md#setrelativerotation)**(`rotation`: [`Rotation`](Type.Rotation.md)): `void` <br> 设置相对旋转|
| **[setRelativeScale](Gameplay.GameObject.md#setrelativescale)**(`scale`: [`Vector`](Type.Vector.md)): `void` <br> 设置相对缩放|
| **[setTransform](Gameplay.GameObject.md#settransform)**(`transform`: [`Transform`](Type.Transform.md)): `void` <br> 设置当前物体transform|
| **[setVisibility](Gameplay.GameObject.md#setvisibility)**(`status`: [`PropertyStatus`](../enums/Type.PropertyStatus.md), `propagateToChildren?`: `boolean`): `void` <br> 设置GameObject是否被显示|
| **[setWorldLocation](Gameplay.GameObject.md#setworldlocation)**(`v`: [`Vector`](Type.Vector.md)): `void` <br> 设置物体的世界坐标|
| **[setWorldRotation](Gameplay.GameObject.md#setworldrotation)**(`rotation`: [`Rotation`](Type.Rotation.md)): `void` <br> 设置物体的世界旋转|
| **[setWorldScale](Gameplay.GameObject.md#setworldscale)**(`v`: [`Vector`](Type.Vector.md)): `void` <br> 设置物体的世界缩放|
| **[asyncFind](Gameplay.GameObject.md#asyncfind)**(`GUID`: `string`): `Promise`<`GameObject`\> <br> 通过GUID异步查找GameObject,默认是五秒,可以通过 `core.setGlobalAsyncOverTime(5000);|
| **[asyncSpawn](Gameplay.GameObject.md#asyncspawn)**<`T`: extends `GameObject`<`T`\>\>(`spawnInfo`: [`SpawnInfo`](../interfaces/Type.SpawnInfo.md)): `Promise`<`T`: extends `GameObject`<`T`\>\> <br> 异步构造一个 GameObject 资源不存在会先去下载资源再去创建|
| **[asyncSpawnGameObject](Gameplay.GameObject.md#asyncspawngameobject)**(`assetId`: `string`, `inReplicates?`: `boolean`, `transform?`: [`Transform`](Type.Transform.md)): `Promise`<`GameObject`\> <br> 异步构造一个 GameObject 资源不存在会先去下载资源再去创建|
| **[find](Gameplay.GameObject.md#find)**(`GUID`: `string`): `GameObject` <br> 通过GUID查找GameObject|
| **[findGameObjectByTag](Gameplay.GameObject.md#findgameobjectbytag)**(`InTag`: `string`): `GameObject`[] <br> 通过自定义Tag获取GameObject|
| **[getGameObjectByName](Gameplay.GameObject.md#getgameobjectbyname)**(`name`: `string`): `undefined` \| `GameObject` <br> 通过名字查找物体|
| **[getGameObjectsByName](Gameplay.GameObject.md#getgameobjectsbyname)**(`name`: `string`): `GameObject`[] <br> 通过名字查找物体|
| **[spawn](Gameplay.GameObject.md#spawn)**<`T`: extends `GameObject`<`T`\>\>(`[spawn](Gameplay.GameObject.md#spawn)Info`): `T`: extends `GameObject`<`T`\> <br> 构造一个 GameObject|
| **[spawnGameObject](Gameplay.GameObject.md#spawngameobject)**(`assetId`: `string`, `inReplicates?`: `boolean`, `transform?`: [`Transform`](Type.Transform.md)): `GameObject` <br> 构造一个 GameObject|
:::


## Properties

### onInteractiveEnded <Score text="onInteractiveEnded" /> 

• **onInteractiveEnded**: [`MulticastDelegate`](Type.MulticastDelegate.md)<() => `void`\>

交互结束时执行绑定函数

::: warning Precautions

会自动广播，若是双端对象，则可以在任意客户端调用

:::

___

### onInteractiveStarted <Score text="onInteractiveStarted" /> 

• **onInteractiveStarted**: [`MulticastDelegate`](Type.MulticastDelegate.md)<() => `void`\>

交互开始时执行绑定函数

::: warning Precautions

会自动广播，若是双端对象，则可以在任意客户端调用

:::

___

### onInteractorEnter <Score text="onInteractorEnter" /> 

• **onInteractorEnter**: [`Delegate`](Type.Delegate.md)<(`result`: `boolean`) => `void`\>

::: danger Deprecated

info:该接口已废弃，在该接口被删除前会仍保持可用，请尽快使用替换方案以免出现问题 since:022 reason: API 注释命名优化 replacement: enterInteractiveState 返回的 promise

:::

（请不要使用此委托，绑定的回调会在调用交互时被重置，外部回调不会触发）激活交互时执行绑定函数

::: warning Precautions

不要使用此委托，直接使用激活函数返回的 Promise 可达到同样的效果

:::

使用示例: 如下示例展示此委托的参数意义和使用方法
```ts
interactor.onInteractorEnter.add((result: boolean) => {
    // 参数 result: 激活交互成功时返回 true
    // 激活交互完成时触发
})
```

___

### onInteractorExit <Score text="onInteractorExit" /> 

• **onInteractorExit**: [`Delegate`](Type.Delegate.md)<(`result`: `boolean`) => `void`\>

::: danger Deprecated

info:该接口已废弃，在该接口被删除前会仍保持可用，请尽快使用替换方案以免出现问题 since:022 reason: API 注释命名优化 replacement: exitInteractiveState 返回的 promise

:::

（请不要使用此委托，绑定的回调会在调用退出交互时被重置，外部回调不会触发）退出交互时执行绑定函数

::: warning Precautions

不要使用此委托，直接使用退出交互函数返回的 Promise 可达到同样的效果

:::

使用示例: 如下示例展示此委托的参数意义和使用方法
```ts
interactor.onInteractorExit.add((result: boolean) => {
    // 参数 result: 退出交互成功时为 true
    // 激活交互完成时触发
})
```

## Accessors

### interactiveSlot <Score text="interactiveSlot" /> 

• `get` **interactiveSlot**(): [`InteractiveSlot`](../enums/Gameplay.InteractiveSlot.md)

交互物插槽

#### Returns

[`InteractiveSlot`](../enums/Gameplay.InteractiveSlot.md)

• `set` **interactiveSlot**(`slot`): `void`

交互物插槽

#### Parameters

| Name | Type |
| :------ | :------ |
| `slot` | [`InteractiveSlot`](../enums/Gameplay.InteractiveSlot.md) |


___

### interactiveStance <Score text="interactiveStance" /> 

• `get` **interactiveStance**(): `string`

交互动画姿态资源 id

#### Returns

`string`

• `set` **interactiveStance**(`assetGuid`): `void`

交互动画姿态资源 id

#### Parameters

| Name | Type |
| :------ | :------ |
| `assetGuid` | `string` |



## Methods

### endInteract <Score text="endInteract" /> 

• **endInteract**(`endLoc?`, `endRot?`, `newStance?`): `boolean` <Badge type="tip" text="other" />

结束交互

调用端自动广播

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `endLoc?` | [`Vector`](Type.Vector.md) |  结束位置 default: 玩家开始交互前的坐标为准 |
| `endRot?` | [`Rotation`](Type.Rotation.md) |  结束旋转量 default: 玩家开始交互前的旋转为准，如果玩家开始前的姿态是倾斜的，内部不会纠正 |
| `newStance?` | `string` |  新姿态，default: 以属性玩家开始交互前的姿态为准 |

#### Returns

`boolean`

true 触发了结束交互逻辑

___

### enterInteractiveState <Score text="enterInteractiveState" /> 

• **enterInteractiveState**(`characterObj`): `Promise`<`boolean`\> <Badge type="tip" text="other" />

::: danger Deprecated

info:该接口已废弃，在该接口被删除前会仍保持可用，请尽快使用替换方案以免出现问题 since:024 reason: 交互物 v1 v2 兼容 replacement: startInteract (请注意，如果需要换为此接口，结束接口也务必更换为 endInteract)

:::

激活交互，将角色切换到特定姿态和位置，并绑定到交互物上

调用端自动广播

::: warning Precautions

双端都可以调用，客户端调用会自动广播到服务端

:::

使用示例: 如下示例展示此方法使用方法和返回的 Promise 的参数意义
```ts
interactor.enterInteractiveState(Gameplay.getCurrentPlayer().character).then((result) => {
    // 参数 result:  激活交互成功时为 true
    // do something
})
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `characterObj` | `GameObject` |  激活交互的角色 default: |

#### Returns

`Promise`<`boolean`\>

将返回是否激活成功的 Promise

___

### exitInteractiveState <Score text="exitInteractiveState" /> 

• **exitInteractiveState**(`Location`, `stance?`): `Promise`<`boolean`\> <Badge type="tip" text="other" />

::: danger Deprecated

info:该接口已废弃，在该接口被删除前会仍保持可用，请尽快使用替换方案以免出现问题 since:024 reason: 交互物 v1 v2 兼容 replacement: endInteract (请注意，如果需要换为此接口，开始接口也务必更换)

:::

退出交互，恢复角色的绑定关系，姿态和位置

调用端自动广播

使用示例: 如下示例展示此方法使用方法和返回的 Promise 的参数意义
```ts
interactor.exitInteractiveState(newLocation, "").then((result) => {
    // 参数 result: 退出交互成功时为 true
    // do something
})
```

::: warning Precautions

双端都可以调用，客户端调用会自动广播到服务端

:::

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `Location` | [`Vector`](Type.Vector.md) |  退出交互的位置 |
| `stance?` | `string` |  退出交互物的姿态 default: undefined |

#### Returns

`Promise`<`boolean`\>

将返回是否退出激活成功的 Promise


### getInteractCharacter <Score text="getInteractCharacter" /> 

• **getInteractCharacter**(): [`CharacterBase`](Gameplay.CharacterBase.md) 

获取正在交互的角色


#### Returns

[`CharacterBase`](Gameplay.CharacterBase.md)

true：为交互中

___

### getInteractiveState <Score text="getInteractiveState" /> 

• **getInteractiveState**(): `boolean` 

::: danger Deprecated

info:该接口已废弃，在该接口被删除前会仍保持可用，请尽快使用替换方案以免出现问题 since:024 reason: 交互物 v1 v2 兼容 replacement: getInteractiveStatus

:::

获取该交互物的交互状态


#### Returns

`boolean`

true: 为交互中

___

### getInteractiveStatus <Score text="getInteractiveStatus" /> 

• **getInteractiveStatus**(): `boolean` 

获取该交互物的交互状态


#### Returns

`boolean`

true：为交互中


### interactiveCharacter <Score text="interactiveCharacter" /> 

• **interactiveCharacter**(): [`Character`](Gameplay.Character.md) 

::: danger Deprecated

info:该接口已废弃，在该接口被删除前会仍保持可用，请尽快使用替换方案以免出现问题 since:024 reason: 交互物 v1 v2 兼容 replacement:

:::

获取和交互物发生交互的角色

**`Precautious`**

不能代替 interactiveState 使用，RPC 传递过程中无法保证此参数更新的准确及时


#### Returns

[`Character`](Gameplay.Character.md)

和交互物发生交互的角色，可能为空


### startInteract <Score text="startInteract" /> 

• **startInteract**(`newCharObj`, `newSlot?`, `newStance?`): `boolean` <Badge type="tip" text="other" />

开始交互

::: warning Precautions

建议客户端调用

:::

调用端自动广播

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `newCharObj` | [`CharacterBase`](Gameplay.CharacterBase.md) |  要交互的角色（可以是玩家，也可以是AI） |
| `newSlot?` | [`InteractiveSlot`](../enums/Gameplay.InteractiveSlot.md) |  交互插槽，不传默认以属性 interactiveSlot 为准 default: 属性 interactiveSlot |
| `newStance?` | `string` |  交互姿态，不传默认以属性 interactiveStance 为准 default: 属性 interactiveStance |

#### Returns

`boolean`

是否成功交互
