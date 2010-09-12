# $NetBSD$
#

DISTNAME=	ChunkFive
PKGNAME=	chunkfive-1
CATEGORIES=	fonts
MASTER_SITES=	http://github.com/downloads/ryo-on/pkgsrc-local/
EXTRACT_SUFX=	.zip

MAINTAINER=	ryo_on@yk.rim.or.jp
HOMEPAGE=	http://www.fontsquirrel.com/fonts/ChunkFive
COMMENT=	Chunk is an ultra-bold slab serif typeface
LICENSE=	open-font-license

PKG_DESTDIR_SUPPORT=	user-destdir

USE_X11BASE=	yes
NO_CONFIGURE=	yes
NO_BUILD=	yes

INSTALLATION_DIRS=	lib/X11/fonts/TTF

FONTDIR=	${PREFIX}/lib/X11/fonts/TTF
FONTS_DIRS.ttf=	${FONTDIR}

INSTALL_FONTS=	Chunkfive.otf

USE_LANGUAGES=	# none

WRKSRC=	${WRKDIR}

do-install:
.for fontfile in ${INSTALL_FONTS}
	${INSTALL_DATA} ${WRKSRC}/${fontfile} ${DESTDIR}${FONTDIR}
.endfor

.include "../../mk/bsd.pkg.mk"
