# Chạy Local 
wrangler pages dev public

# Triển khai lên Cloudflare Pages
wrangler pages deploy public
wrangler pages deploy --project-name=dictqq
> `functions` là thư mục

# Đăng nhập vào Cloudflare (nếu chưa đăng nhập)
wrangler login

# Xóa alias cũ
wrangler pages domain delete master.yaozu.pages.dev

# Đặt domain mới làm primary
wrangler pages domain set-primary yaozu.pages.dev
wrangler pages deploy functions --project-name=yaozu --branch=main
