PRINTF_DIR = printf
PRINTF = $(PRINTF_DIR)/printf.a
GNL = $(GNL_DIR)/get_next_line
GNL = GNL_DIR
SRC	 =	ft_isalnum.c ft_isprint.c ft_memcmp.c  ft_putchar_fd.c ft_split.c 	\
	ft_strlcat.c ft_strncmp.c ft_substr.c ft_atoi.c ft_isalpha.c 			\
	ft_itoa.c ft_memcpy.c  ft_putendl_fd.c ft_strchr.c  ft_strlcpy.c 		\
	ft_strnstr.c ft_tolower.c ft_bzero.c   ft_isascii.c 			 		\
	ft_memmove.c ft_putnbr_fd.c  ft_strdup.c  ft_strlen.c  ft_strrchr.c 	\
	ft_toupper.c ft_calloc.c  ft_isdigit.c ft_memchr.c  ft_memset.c  		\
	ft_putstr_fd.c  ft_strjoin.c ft_strmapi.c ft_strtrim.c ft_striteri.c	\
OBJ = $(SRC:.c=.o)
BONUS = ft_lstnew.c	ft_lstadd_front.c ft_lstsize.c ft_lstlast.c \
	ft_lstclear.c ft_lstdelone.c ft_lstadd_back.c ft_lstiter.c \
	ft_lstmap.c 
BONUS_OBJ = $(BONUS:.c=.o)
NAME = libft.a
FLAGS = -Wall -Wextra -Werror
CC = cc
HEADER = libft.h

all: $(NAME)

$(NAME): $(PRINTF) $(GNL)
	$(CC) $(FLAGS) -c $(SRC)
	ar rcs $(NAME) $(OBJ)

main: all
	$(CC) $(FLAGS) -L. $(NAME)

$(PRINTF):
	$(MAKE) -C $(PRINTF_DIR)

$(GNL)
	$(MAKE) -C (GNL_DIR)

clean:
	rm -rf $(OBJ) $(BONUS_OBJ)
	$(MAKE) -C $(PRINTF_DIR) clean
	$(MAKE) -C $(GNL_DIR) clean

fclean: clean
	rm -f $(NAME) a.out
	$(MAKE) -C $(PRINTF_DIR) fclean
	$(MAKE) -C $(GNL_DIR) fclean

re: fclean all

bonus: $(OBJ) $(BONUS_OBJ)
	ar rcs $(NAME) $(OBJ) $(BONUS_OBJ)

.PHONY:			all clean fclean re bonus