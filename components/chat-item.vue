<template name="chat-item">
    <view class="chat-item-style" @longtap="onConversationLongTap" @tap="chatTo" :data-item="item" hover-class="press-style">
        <template is="chat-item-head" :data="headUrl:item.ui.portrait,unread:item.ui.unread"></template>
        <view class="chat-item-content-super-style">
            <view class="chat-item-name-style">{{item.ui.title}}</view>
            <!-- <view class="chat-item-name-style">targetName</view> -->
            <!-- <image src="./../../image/chat/send_fail.png" style="width: 28rpx;height: 28rpx;margin-right: 6rpx;"/> -->
            <text class="chat-item-content-style">{{item.ui.lastMsgContent}}</text>
        </view>
        <view class="chat-item-status-super-style">
            <view class="chat-item-time-style">{{item.ui.time}}</view>
        </view>
    </view>
    <view class="list-divide-line" style="width: 79.5%;margin-left: 20.5%"></view>
</template>