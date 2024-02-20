# WEB-APP

# 命名規約（nuxt）
### components/
- パスカルケースで統一（例: UserProfileCard.vue）
- 類似の機能を持つコンポーネントは、プレフィックスでグループ化（例: BaseButton.vue, BaseInput.vue）

### pages/
- ファイル名はケバブケース（例: user-profile.vue）
- 動的なページを表すファイル名は、プレフィックスとして_を使用（例: _id.vue）。
- 特定のディレクトリのルートページはindex.vue

## タグ内の記述順
- ディレクティブの順番: v-if, v-for, v-model, v-on（@）, v-bind（:）の順番で記述
例：<div v-if="isVisible" v-for="item in items" :key="item.id" @click="handleClick" :class="{'is-active': isActive}"></div>

- 属性の順番: 標準のHTML属性（例: class, id, name）、ディレクティブ、その他の属性（type, hrefなど）の順に記述
例：<input class="form-control" id="email" name="email" v-model="email" type="email" placeholder="Enter your email">

# コンテナの立ち上げ
    - docker-compose up -d

# コンテナの停止・削除
    - docker-compose down