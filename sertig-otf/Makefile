# $NetBSD$
#

DISTNAME=	Sertig___Free_Font_by_Dannci
PKGNAME=	sertig-1
CATEGORIES=	fonts
MASTER_SITES=	http://www.deviantart.com/download/162037602/
EXTRACT_SUFX=	.zip

MAINTAINER=	ryo_on@yk.rim.or.jp
HOMEPAGE=	http://typethefont.com/post/550992450/sertig-free-font
COMMENT=	Free sans-serif font
LICENSE=	open-font-license

PKG_DESTDIR_SUPPORT=	user-destdir

USE_X11BASE=	yes
NO_CONFIGURE=	yes
NO_BUILD=	yes

INSTALLATION_DIRS=	lib/X11/fonts/TTF

FONTDIR=	${PREFIX}/lib/X11/fonts/TTF
FONTS_DIRS.ttf=	${FONTDIR}

INSTALL_FONTS=	Sertig.otf

USE_LANGUAGES=	# none

WRKSRC=	${WRKDIR}

do-install:
.for fontfile in ${INSTALL_FONTS}
	${INSTALL_DATA} ${WRKSRC}/${fontfile} ${DESTDIR}${FONTDIR}
.endfor

.include "../../mk/bsd.pkg.mk"
