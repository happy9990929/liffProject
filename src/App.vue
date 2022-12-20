<script setup>
import { onMounted, reactive } from "@vue/runtime-core";
import liff from "@line/liff";

const liffInfo = reactive({
  data: {
    OS: "",
    language: "",
    version: "",
    lineVersion: "",
    context: "",
    isInClient: "",
    isLoggedIn: "",
  },
});

const sendMsg = () => {
  liff
    .sendMessages([
      {
        type: "image",
        originalContentUrl:
          "https://raw.githubusercontent.com/happy9990929/react-lazy-load/main/src/images/dog.jpg",
        previewImageUrl:
          "https://raw.githubusercontent.com/happy9990929/react-lazy-load/main/src/images/dog-placeholder.jpg",
      },
      {
        type: "video",
        originalContentUrl: "https://i.imgur.com/vtUbRV6.mp4",
        previewImageUrl:
          "https://raw.githubusercontent.com/happy9990929/react-lazy-load/main/src/images/dog-placeholder.jpg",
        trackingId: "track-id",
      },
      {
        type: "location",
        title: "波比公園",
        address: "台中市龍井區東風門市",
        latitude: 24.191236,
        longitude: 120.587724,
      },
      {
        type: "template",
        altText: "this is a confirm template",
        template: {
          type: "confirm",
          text: "波比要吃什麼?",
          actions: [
            {
              type: "uri",
              label: "雞腿",
              uri: "http://example.com/page/123",
            },
            {
              type: "uri",
              label: "罐罐",
              uri: "http://example.com/page/123",
            },
          ],
        },
      },
      {
        type: "flex",
        altText: "this is a flex message",
        contents: {
          type: "bubble",
          hero: {
            type: "image",
            url: "https://raw.githubusercontent.com/happy9990929/react-lazy-load/main/src/images/dog.jpg",
            size: "full",
            aspectRatio: "20:13",
            aspectMode: "cover",
            action: {
              type: "uri",
              uri: "http://linecorp.com/",
            },
          },
          body: {
            type: "box",
            layout: "vertical",
            contents: [
              {
                type: "text",
                text: "Brown Cafe",
                weight: "bold",
                size: "xl",
              },
              {
                type: "box",
                layout: "baseline",
                margin: "md",
                contents: [
                  {
                    type: "icon",
                    size: "sm",
                    url: "https://scdn.line-apps.com/n/channel_devcenter/img/fx/review_gold_star_28.png",
                  },
                  {
                    type: "icon",
                    size: "sm",
                    url: "https://scdn.line-apps.com/n/channel_devcenter/img/fx/review_gold_star_28.png",
                  },
                  {
                    type: "icon",
                    size: "sm",
                    url: "https://scdn.line-apps.com/n/channel_devcenter/img/fx/review_gold_star_28.png",
                  },
                  {
                    type: "icon",
                    size: "sm",
                    url: "https://scdn.line-apps.com/n/channel_devcenter/img/fx/review_gold_star_28.png",
                  },
                  {
                    type: "icon",
                    size: "sm",
                    url: "https://scdn.line-apps.com/n/channel_devcenter/img/fx/review_gray_star_28.png",
                  },
                  {
                    type: "text",
                    text: "4.0",
                    size: "sm",
                    color: "#999999",
                    margin: "md",
                    flex: 0,
                  },
                ],
              },
              {
                type: "box",
                layout: "vertical",
                margin: "lg",
                spacing: "sm",
                contents: [
                  {
                    type: "box",
                    layout: "baseline",
                    spacing: "sm",
                    contents: [
                      {
                        type: "text",
                        text: "Place",
                        color: "#aaaaaa",
                        size: "sm",
                        flex: 1,
                      },
                      {
                        type: "text",
                        text: "Miraina Tower, 4-1-6 Shinjuku, Tokyo",
                        wrap: true,
                        color: "#666666",
                        size: "sm",
                        flex: 5,
                      },
                    ],
                  },
                  {
                    type: "box",
                    layout: "baseline",
                    spacing: "sm",
                    contents: [
                      {
                        type: "text",
                        text: "Time",
                        color: "#aaaaaa",
                        size: "sm",
                        flex: 1,
                      },
                      {
                        type: "text",
                        text: "10:00 - 23:00",
                        wrap: true,
                        color: "#666666",
                        size: "sm",
                        flex: 5,
                      },
                    ],
                  },
                ],
              },
            ],
          },
          footer: {
            type: "box",
            layout: "vertical",
            spacing: "sm",
            contents: [
              {
                type: "button",
                style: "link",
                height: "sm",
                action: {
                  type: "uri",
                  label: "CALL",
                  uri: "https://linecorp.com",
                },
              },
              {
                type: "button",
                style: "link",
                height: "sm",
                action: {
                  type: "uri",
                  label: "WEBSITE",
                  uri: "https://linecorp.com",
                },
              },
              {
                type: "box",
                layout: "vertical",
                contents: [],
                margin: "sm",
              },
            ],
            flex: 0,
          },
        },
      },
    ])
    .then(function (res) {
      console.log(res);
    })
    .catch(function (error) {
      console.log(error);
    });
};

const sendMsg2 = () => {
  liff
    .sendMessages([
      {
        type: "flex",
        altText: "12/21廢物生日派對",
        contents: {
          type: "carousel",
          contents: [
            {
              type: "bubble",
              body: {
                type: "box",
                layout: "vertical",
                contents: [
                  {
                    type: "image",
                    url: "https://happy9990929.github.io/liffProject/1.jpg",
                    size: "full",
                    aspectMode: "cover",
                    aspectRatio: "2:3",
                    gravity: "top",
                  },
                  {
                    type: "box",
                    layout: "vertical",
                    contents: [
                      {
                        type: "box",
                        layout: "vertical",
                        contents: [
                          {
                            type: "text",
                            text: "每年的12/21",
                            size: "xl",
                            color: "#ffffff",
                            weight: "bold",
                          },
                        ],
                      },
                      {
                        type: "box",
                        layout: "baseline",
                        contents: [
                          {
                            type: "text",
                            text: "廢倫誕辰日",
                            color: "#ebebeb",
                            size: "sm",
                            flex: 0,
                          },
                        ],
                        spacing: "lg",
                      },
                    ],
                    position: "absolute",
                    offsetBottom: "0px",
                    offsetStart: "0px",
                    offsetEnd: "0px",
                    backgroundColor: "#03303Acc",
                    paddingAll: "20px",
                    paddingTop: "18px",
                  },
                  {
                    type: "box",
                    layout: "vertical",
                    contents: [
                      {
                        type: "text",
                        text: "廢物",
                        color: "#ffffff",
                        align: "center",
                        size: "xs",
                        offsetTop: "3px",
                      },
                    ],
                    position: "absolute",
                    cornerRadius: "20px",
                    offsetTop: "18px",
                    backgroundColor: "#ff334b",
                    offsetStart: "18px",
                    height: "25px",
                    width: "53px",
                  },
                ],
                paddingAll: "0px",
              },
            },
            {
              type: "bubble",
              body: {
                type: "box",
                layout: "vertical",
                contents: [
                  {
                    type: "image",
                    url: "https://happy9990929.github.io/liffProject/3.jpg",
                    size: "full",
                    aspectMode: "cover",
                    aspectRatio: "2:3",
                    gravity: "top",
                  },
                  {
                    type: "box",
                    layout: "vertical",
                    contents: [
                      {
                        type: "box",
                        layout: "vertical",
                        contents: [
                          {
                            type: "text",
                            text: "永遠都會有我對你說聲:)",
                            size: "xl",
                            color: "#ffffff",
                            weight: "bold",
                          },
                        ],
                      },
                      {
                        type: "box",
                        layout: "baseline",
                        contents: [
                          {
                            type: "text",
                            text: "🐭🐭🐭",
                            color: "#ebebeb",
                            size: "sm",
                            flex: 0,
                          },
                        ],
                        spacing: "lg",
                      },
                    ],
                    position: "absolute",
                    offsetBottom: "0px",
                    offsetStart: "0px",
                    offsetEnd: "0px",
                    backgroundColor: "#9C8E7Ecc",
                    paddingAll: "20px",
                    paddingTop: "18px",
                  },
                  {
                    type: "box",
                    layout: "vertical",
                    contents: [
                      {
                        type: "text",
                        text: "廢渣",
                        color: "#ffffff",
                        align: "center",
                        size: "xs",
                        offsetTop: "3px",
                      },
                    ],
                    position: "absolute",
                    cornerRadius: "20px",
                    offsetTop: "18px",
                    backgroundColor: "#ff334b",
                    offsetStart: "18px",
                    height: "25px",
                    width: "53px",
                  },
                ],
                paddingAll: "0px",
              },
            },
            {
              type: "bubble",
              body: {
                type: "box",
                layout: "vertical",
                contents: [
                  {
                    type: "image",
                    url: "https://happy9990929.github.io/liffProject/4.jpg",
                    size: "full",
                    aspectMode: "cover",
                    aspectRatio: "2:3",
                    gravity: "top",
                  },
                  {
                    type: "box",
                    layout: "vertical",
                    contents: [
                      {
                        type: "box",
                        layout: "vertical",
                        contents: [
                          {
                            type: "text",
                            text: "眼睛可以張開嗎廢物！！",
                            size: "xl",
                            color: "#ffffff",
                            weight: "bold",
                          },
                        ],
                      },
                      {
                        type: "box",
                        layout: "baseline",
                        contents: [
                          {
                            type: "text",
                            text: "廢物生日快樂🥳",
                            color: "#ebebeb",
                            size: "sm",
                            flex: 0,
                          },
                        ],
                        spacing: "lg",
                      },
                    ],
                    position: "absolute",
                    offsetBottom: "0px",
                    offsetStart: "0px",
                    offsetEnd: "0px",
                    backgroundColor: "#03303Acc",
                    paddingAll: "20px",
                    paddingTop: "18px",
                  },
                  {
                    type: "box",
                    layout: "vertical",
                    contents: [
                      {
                        type: "text",
                        text: "廢到爆",
                        color: "#ffffff",
                        align: "center",
                        size: "xs",
                        offsetTop: "3px",
                      },
                    ],
                    position: "absolute",
                    cornerRadius: "20px",
                    offsetTop: "18px",
                    backgroundColor: "#ff334b",
                    offsetStart: "18px",
                    height: "25px",
                    width: "53px",
                  },
                ],
                paddingAll: "0px",
              },
            },
          ],
        },
      },
    ])
    .catch((error) => {
      alert(error);
    });
};

const liffInit = async () => {
  const liffId = import.meta.env.VITE_LIFF_ID;

  try {
    await liff.init({ liffId: liffId });
    liffInfo.data.OS = liff.getOS();
    liffInfo.data.language = liff.getLanguage();
    liffInfo.data.version = liff.getVersion();
    liffInfo.data.lineVersion = liff.getLineVersion();
    liffInfo.data.context = liff.getContext();
    liffInfo.data.isLoggedIn = liff.isLoggedIn();
    var user = liff.getDecodedIDToken();
    console.log(user);
    console.log(liffInfo.data.isLoggedIn);

    liff.getFriendship().then((data) => {
      if (data.friendFlag) {
        console.log(data);
      }
    });

    // if (!liffInfo.data.isLoggedIn) {
    //   liff.login();
    // }

    sendMsg2();
    // liff.scanCodeV2().then((result) => {
    //   alert('scanCodeV2')
    // })
    // .catch((error) => {
    //   console.log("error", error);
    // });
  } catch (err) {
    alert(err);
  }
};

const closeLiff = () => {
  liff.closeWindow()
}

onMounted(() => {
  liffInit();
});
</script>

<template>
  <div>
    <!-- 作業系統: {{liffInfo.data.OS}}<br>
    語系: {{liffInfo.data.language}}<br>
    SDK 版本: {{liffInfo.data.version}}<br>
    Line 版本: {{liffInfo.data.lineVersion}}<br>
    isInClient: {{liffInfo.data.isInClient}}<br>
    isLoggedIn: {{liffInfo.data.isLoggedIn}}<br> -->
    <img src="./assets/error.png" alt="">
    <h1>恭喜您已中毒！</h1>
    <button type="button" class="btn" @click="closeLiff">點我即可解除木馬</button>
  </div>
</template>

<style scoped>
.btn {
  background-color: #35a983;
  color: #FFF;
  font-size: 1.5rem;
  font-weight: bold;
}
</style>
