<template>
    <li>
        <slot>
            <!-- 부모에서 정의할 화면 영역 -->
        </slot>
        <!-- 이름있는 슬롯 -->
        <slot name="header">
              <div>
                  default header
              </div>
        </slot>
    </li>
</template>
