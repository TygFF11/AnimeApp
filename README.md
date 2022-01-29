# README


# users
|  Column              |  Type          |  Options                        |
|  name                |  string        |  null: false                    |
|  email               |  string        |  null: false                    |
|  encrypted_password  |  string        |  null: false                    |

- has_many :user_threads
- has_many :threads through: :user_threads
- has_many :comments


# user_threads
|  Column              |  Type           |  Options                        |
|  user                |  references     |  null: false, foreign_key: true |
|  thread              |  references     |  null: false, foreign_key: true |

- belongs_to :user
- belongs_to :thread


# threads
|  Column              |  Type           |  Options                        |
|  name                |  string         |  null: false                    |

- has_many :user_threads
- has_many :users through: :user_threads
- has_many :comments


# comments
|  Column              |  Type           |  Options                        |
|  content             |  string         |  null: false                    |
|  user                |  references     |  null: false, foreign_key: true |
|  thread              |  references     |  null: false, foreign_key: true |

- belongs_to :user
- belongs_to :thread


# favorites
|  Column              |  Type           |  Options                        |



